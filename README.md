# wordpress-security-settings

WordPress Security & Performance Settings

## FTP

● Set permission to 755 for folders
● Set permission to 644 for files

## wp-config.php

● Add: define('DISALLOW_FILE_EDIT', true);
● Renew security-keys
● Change wp table prefix

## Plugins

### Security

● wpcrapremove
● WPS Hide Login
● jQuery Updater
● Wordfence Security
● Contact Form 7: reCAPTCHA v3

### Performance

● Autoptimize
● a3 Lazy Load
● WP Fastest Cache
● Super Progressive Web Apps

### Better Workflow

● Disable Gutenberg
● Duplicate Post

### Troubleshooting

● Query Monitor
● Health Check & Troubleshooting

### SEO & Analytics

● Yoast SEO
● Site Kit by Google

## WP-Admin

### Settings

#### Global

● Membership: “Everyone can register.” -> OFF
● New user's default role: “Subscriber”

#### Write

● Update Services -> Remove All

#### Discussion

##### Default settings for posts

● “Try to access every weblog linked in posts notify (slows publishing) ”-> OFF

● “Link notifications from other blogs (pingbacks and Enable trackbacks) for new posts ”-> OFF

##### More comment settings

● “Users must be registered and logged in to comment” -> ON

##### Before a comment appears

● “The comment must be released manually.” -> ON

##### Avatar display

● “Show avatars” -> OFF

## .htaccess

https://github.com/h5bp/server-configs-apache/blob/master/dist/.htaccess

+

<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteCond %{REQUEST_METHOD} ^TRACE RewriteRule .* - [F]
</IfModule>

<ifModule mod_headers.c>
    Header set Connection keep-alive
</ifModule>

<Files ~ "^.*\.([Hh][Tt][Aa])">
    order deny,allow
    deny from all
</Files>

<Files xmlrpc.php>
    order deny,allow deny from all
</Files>

<Files wp-config.php>
    order deny,allow deny from all
</Files>

<Files wp-config-sample.php>
    order deny,allow
deny from all
</Files>

<Files license.txt>
    order deny,allow deny from all
</Files>

<Files liesmich.html>
    order deny,allow deny from all
</Files>

<Files readme.html>
    order deny,allow deny from all
</Files>

<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteCond %{HTTPS} !=on
    RewriteRule ^ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
</IfModule>

<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteCond %{HTTP_HOST} !^www\.
    RewriteRule ^(.*)$ https://www.%{HTTP_HOST}/$1 [R=301,L]
</IfModule>
