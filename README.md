Change Password
===============

This is a [YOURLS](http://yourls.org/) plugin to allow users to change their password via the administration interface and stores a hashed version in the configuration file. You can enforce minimum length and some complexity requirements.

Requirements
------------
- YOURLS version 1.7 or greater
- Passwords must already be hashed by YOURLS

Installation
------------
- In `/user/plugins` create a directory named `change-password`
- Copy these files to that directory
- Activate this plugin on the manage plugins page

Configuration
-------------
By default this plugin enforces a minimum password length of 6 characters. You can change that and also enforce any of the following:
- Require at least one digit
- Require at least one special character
- Require both uppercase and lowercase letters
 
Place the following directives at the end of `config.php` and change them to meet your needs:
```
/**
 * Settings for Change Password plugin
 */
 define('VVA_CHANGE_PASSWORD_MINIMUM_LENGTH', 6 );
 define('VVA_CHANGE_PASSWORD_USE_DIGITS', FALSE );
 define('VVA_CHANGE_PASSWORD_USE_SPECIAL', FALSE );
 define('VVA_CHANGE_PASSWORD_USE_UPPERCASE', FALSE );
```

Notes
-----
If a new version of YOURLS implements user management in the database this plugin will be obsolete. This is intended as a workaround until then.

Version
-------
1.0

Source
------
https://github.com/vvanasten/YOURLS-Change-Password

License
-------
MIT