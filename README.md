[![Codefresh build status]( https://g.codefresh.io/api/badges/pipeline/arm_alpha/ruanbekker%2Fcf-armhf-apache-php%2Fcf-armhf-apache-php?branch=master&key=eyJhbGciOiJIUzI1NiJ9.NWI0NGRjNmExZDVkMDYwMDAxZDI4NWJl.npctK3AbmWlwYzvnK_U6qv-4XBNMqrEyCoGVbFPeMjY&type=cf-1)]( https://g.codefresh.io/repositories/ruanbekker/cf-armhf-apache-php/builds?filter=trigger:build;branch:master;service:5b72e51aaedcd03c1eccbe2b~cf-armhf-apache-php)

# cf-armhf-apache-php
Apache and PHP5 on ARM

## Version Info

Default:
- Alpine: 3.8
- Apache: 2.4.33
- PHP: 5.6

## Web Content

Content should be placed under the `htdocs` directory which will be shipped to `/var/www/localhost/htdocs` inside the container.

`index.php` will be looked up first, then `index.html`

## Usage

The image contains a `index.php` that displays the hostname of the container.

Spin up a container:

```
$ docker run -it -p 80:80 rbekker87/armhf-apache-php:5.6
```

Make a GET request:

```
$ curl -i http://192.168.0.2/
HTTP/1.1 200 OK
Date: Tue, 14 Aug 2018 14:18:48 GMT
Server: Apache/2.4.33 (Unix)
X-Powered-By: PHP/5.6.37
Content-Length: 27
Content-Type: text/html; charset=UTF-8

My Hostname: 4d70857d1946
```
