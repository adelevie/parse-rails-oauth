# About

This is a simple Rails 3.1 app that makes it easy to link OAuth APIs to Parse user accounts.

If you just want a Rails app with a Parse auth system, and no OAuth, check out [parse-rails-boilerplate](http://github.com/adelevie/parse-rails-boilerplate). This project is based on it.

This app uses [parse_resource](http://github.com/adelevie/parse_resource) for model persistence and includes a simple auth system that's based on this [Railscast](http://asciicasts.com/episodes/250-authentication-from-scratch).

If you already use Parse, this Rails app is a really quick way to give your app a web presence.

## Installation

`git clone git@github.com:adelevie/parse-rails-oauth.git`

`cd parse-rails-oauth`

Change application names where necessary, if desired.

[Edit your git](http://stackoverflow.com/questions/2420056/whats-the-best-way-to-replace-remote-origin-url-in-git) configuration so you have a new remote.

`bundle install`

Create a `parse_resource.yml` file. Instructions [here](https://github.com/adelevie/parse_resource/blob/master/README.md).

Read up on [OmniAuth](https://github.com/intridea/omniauth). It's pretty awesome.

Add the appropriate strategies and API keys to `config/initializers/omniauth.rb`. I've included Dropbox (just use your own API keys). Take a look at `app/models/user.rb`. The method `User#dropbox_client` shows a simple implementation of using a client library with this project.

`rails s` and enjoy.

