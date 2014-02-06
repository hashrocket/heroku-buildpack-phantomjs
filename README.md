Heroku buildpack: PhantomJS
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of PhantomJS(http://phantomjs.org).

Using with Ruby/Rails
-----

Add an multi-buildpack to you app:
```shell
$ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi
```

Add `.buildpacks` file to the root of your app containing this:
```
https://github.com/hashrocket/heroku-buildpack-phantomjs
https://github.com/heroku/heroku-buildpack-ruby
```

Modify config variables:
```shell
heroku config:add PATH="/usr/local/bin:/usr/bin:/bin:/app/vendor/phantomjs/bin"
heroku config:add LD_LIBRARY_PATH="/usr/local/lib:/usr/lib:/lib:/app/vendor/phantomjs/lib"
```
