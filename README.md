# wordpress-security-settings

WordPress Security & Performance Settings

## FTP

- Set permission to 755 for folders
- Set permission to 644 for files

## wp-config.php

- Add: define('DISALLOW_FILE_EDIT', true);
- Renew security-keys
- Change wp table prefix

## Plugins

### Security

- wpcrapremove
- WPS Hide Login
- jQuery Updater
- Wordfence Security
- Contact Form 7: reCAPTCHA v3

### Performance

- Autoptimize
- a3 Lazy Load
- WP Fastest Cache
- Super Progressive Web Apps

### Better Workflow

- Disable Gutenberg
- Duplicate Post

### Troubleshooting

- Query Monitor
- Health Check & Troubleshooting

### SEO & Analytics

- Yoast SEO
- Site Kit by Google

## WP-Admin

### Settings

#### Global

- Membership: “Everyone can register.” -> OFF
- New user's default role: “Subscriber”

#### Write

- Update Services -> Remove All

#### Discussion

##### Default settings for posts

- “Try to access every weblog linked in posts notify (slows publishing) ”-> OFF
- “Link notifications from other blogs (pingbacks and Enable trackbacks) for new posts ”-> OFF

##### More comment settings

- “Users must be registered and logged in to comment” -> ON

##### Before a comment appears

- “The comment must be released manually.” -> ON

##### Avatar display

- “Show avatars” -> OFF

## .htaccess

https://github.com/h5bp/server-configs-apache/blob/master/dist/.htaccess
