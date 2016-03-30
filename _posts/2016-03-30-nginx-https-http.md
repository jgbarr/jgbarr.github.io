---
layout: post
title: Nginx redirect from https to http
---
To redirect from https to http (thought the reasons for wanting to do so may be unclear), you can do it this way:
 1. Provision a secure certificate
 2. Aadd this rule into Nginx
<pre><code>
```server {
    listen 443;
    ssl on;
    ssl_certificate /path/to/example.pem;
    ssl_certificate_key /path/to/example.key;
    server_name ~^(www\.)?example\.com$;
    return 301 http://$http_host$request_uri;
  }
```
</code></pre>

-----
