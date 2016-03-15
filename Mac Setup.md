#Dev Environment Set Up


[Setting up a local web server on OS X](https://discussions.apple.com/docs/DOC-3083)

```
1. mkdir ~/Sites

2. sudo vi /etc/apache2/httpd.conf

Uncomment the following lines:
LoadModule php5_module libexec/apache2/libphp5.so
LoadModule userdir_module libexec/apache2/mod_userdir.so
Include /private/etc/apache2/extra/httpd-userdir.conf

3. sudo vi /etc/apache2/extra/httpd-userdir.conf

Uncomment the following lines:
Include /private/etc/apache2/users/*.conf

4. sudo vi /etc/apache2/users/<your short user name>.conf

Use this content:
<Directory "/Users/<your short user name>/Sites/">
    AddLanguage en .en
    LanguagePriority en fr de
    ForceLanguagePriority Fallback
    Options Indexes MultiViews
    AllowOverride None
    Order allow,deny
    Allow from localhost
     Require all granted
</Directory>

5. sudo launchctl load -w /System/Library/LaunchDaemons/org.apache.httpd.plist

6. sudo apachectl restart 
```

[Node Version Manager - NVM](https://github.com/creationix/nvm)

```
git clone https://github.com/creationix/nvm.git ~/.nvm

vim ~/.zshrc
add: . ~/.nvm/nvm.sh

nvm install 4.0.0
nvm use 4.0.0

nvm install iojs

```

[Bootstrap](getbootstrap.com)

```
mkdir <folder>
cd <folder>
mkdir node_module

npm install jquery --save
npm install bootstrap --save

create: js/main.js
add:
var $ = require('jquery');
window.$ = $;
require('bootstrap');
include main.js in index.html

```