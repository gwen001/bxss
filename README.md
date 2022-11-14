# bxss

My alternative to [XSS Hunter](https://xsshunter.com/).
Basically a self hosted PHP script.

<img src="https://raw.githubusercontent.com/gwen001/bxss/main/preview.png" />

## Install

```bash
cd <your_webroot_directory> # cd /var/www/html/x.example.com/
git clone https://github.com/gwen001/bxss
```

The web user should have write access on the directory `images`.

## Apache

Using Apache, you can configure a vhost like this:

```
<IfModule mod_ssl.c>
<VirtualHost *:443>
	ServerName x.example.com
	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html/x.example.com/
	SSLCertificateFile /etc/letsencrypt/live/x.example.com/fullchain.pem
	SSLCertificateKeyFile /etc/letsencrypt/live/x.example.com/privkey.pem
</VirtualHost>
</IfModule>

<VirtualHost *:80>
	ServerName x.example.com
	ServerAdmin webmaster@localhost
	DocumentRoot /var/www/html/x.example.com/
</VirtualHost>
```
