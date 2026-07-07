---
reviewed: 2026-07-07
reviewer: fl
title: HTTPS troubleshooting
naviTitle: HTTPS troubleshooting
navigation.excerpt: Debugging SSL/TLS errors
figure:
  emoji: 🔒
  text: Debug SSL certificate issues.
  color: rgb(34, 197, 94)
  textColor: rgb(220, 252, 231)
lead: Are you seeing a certificate error in the browser? This article helps troubleshoot TLS certificate errors on fortrabbit-hosted domains.
head:
  meta:
    - name: keywords
      content: 'HTTPS certificate error, SSL/TLS troubleshooting, certificate warning, mixed content, fortrabbit'
---

TLS certificates are provided for all [domains](/1.platform/10.objects/10.domain.md). See the [HTTPS article](/1.platform/13.dns/06.https.md) for general features and configuration.

## Review certificates in the browser

Viewing the certificate details in your browser is the first step to diagnosing TLS/SSL issues. In Chrome and Firefox:

1. open `https://www.{{domain}}.com` (use https, not http)
2. click on the lock icon
3. click on certificate to reveal the details

## You see a certificate warning

When visiting your domain under `https://` and the browser shows a certificate error, check the certificate details in the browser. You may see that the cert is issued for `*.frbit.app` rather than your domain. A common error is:

```raw
NET::ERR_CERT_COMMON_NAME_INVALID
```

This can happen if the domain is brand new and the certificate hasn't been installed yet. Certificates typically take up to 24 hours to provision; apex domain certificates often take longer.

It can also occur if your domain isn't yet routed to fortrabbit. Only domains routed to fortrabbit receive TLS certificates. Check the [domain settings](/1.platform/10.objects/10.domain.md) in the dashboard to verify routing.

CAA DNS records can also cause certificate provisioning issues if they restrict certificate issuance. See [HTTPS](/1.platform/13.dns/06.https.md) for details on DNS configuration.

## The browser shows a mixed content warning

When the certificate is installed but you see an error like this, the page contains insecure resources:

> Mixed Content: The page at '{{domain}}' was loaded over HTTPS, but requested an insecure XMLHttpRequest endpoint '{{domain}}'. This request has been blocked; the content must be served over HTTPS.

The issue is that your website requests external resources via http rather than https. This can be CSS files, fonts, images, or AJAX calls. Check your source code for all `http://` requests and replace them.

You have two options: use `https://` explicitly, or omit the protocol entirely with `//`, which uses the same scheme as the current page. The latter approach is especially useful for code that runs in different environments, such as when your local development machine doesn't support TLS.

## Solve SSL verification errors

When your application fails to verify SSL certificates with errors like the following, you need to configure the CA certificate path:

```raw
error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate verify failed
```

You need to set the `capath` as well. Assuming you are using PHP streams, it would look like this:

```php
$context = stream_context_create();
stream_context_set_option($context, 'ssl', 'verify_peer', true);
stream_context_set_option($context, 'ssl', 'capath', '/etc/ssl/certs'); # <<< that's the one
stream_context_set_option($context, 'ssl', 'allow_self_signed', false);

$fp = stream_socket_client("thedomain.tld:443", $errno, $errstr, 5, STREAM_CLIENT_CONNECT, $context);
# ..
if (stream_socket_enable_crypto($fp, true, STREAM_CRYPTO_METHOD_TLS_CLIENT) === false) {
    die("Failed to verify certificate");
}
#...
```

For cURL, the option `CURLOPT_CAPATH` needs to be set to `/etc/ssl/certs`.
