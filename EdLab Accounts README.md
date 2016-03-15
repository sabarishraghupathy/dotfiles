# EdLab Accounts Authentication Project

###Uses: Bootstrap + Jade + Compass + Grunt



##[Compass](http://compass-style.org/install/)
###Install
```
$ gem install compass
```

##[Bootstrap-SASS](https://github.com/twbs/bootstrap-sass)

###Install the gem
```
$ gem install bootstrap-sass
```
###Create new Compass project with bootstrap-sass support
```
$ bundle exec compass create my-new-project -r bootstrap-sass --using bootstrap
```
###If existing Compass project
####Require bootstrap-sass in config.rb:
```
require 'bootstrap-sass'
```
####Install Bootstrap with:
```
$ compass create edlab-accounts -r bootstrap-sass --using bootstrap
```

##[Grunt](http://compass-style.org/install/)
####Create package.json file:
```
npm init
```
####Install Grunt with:
```
$ npm install -g grunt-cli

$ npm install grunt --save-dev

$ npm install grunt-contrib-jade --save-dev

$ npm install grunt-contrib-compass --save-dev

$ npm install grunt-contrib-watch --save-dev
```
####Grunt Watch
```
grunt watch
```