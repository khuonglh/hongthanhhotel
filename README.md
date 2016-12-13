# Hồng Thanh Hotel Management System

[![Build Status](https://semaphoreci.com/api/v1/khuonglh/hongthanhhotel/branches/master/shields_badge.svg)](https://semaphoreci.com/khuonglh/hongthanhhotel)
[![Test Coverage](https://codeclimate.com/github/khuonglh/hongthanhhotel/badges/coverage.svg)](https://codeclimate.com/github/khuonglh/hongthanhhotel/coverage)
[![Code Climate](https://codeclimate.com/github/khuonglh/hongthanhhotel/badges/gpa.svg)](https://codeclimate.com/github/khuonglh/hongthanhhotel)

## Project description

- Front-end webpage:
	+ Introduction hotel
	+ Client Booking
	+ Promotion program (last booking)
- Back-end webpage
	+ Confirmation booking
	+ Check-in/Check-out
	+ Service in house
	+ Billing
	+ CRM


## Dependencies

* PostgreSQL 9.3
* Ruby 2.2.3
* PhantomJS
* Rails 4

Setup required dependencies from `Brewfile`:
```bash
brew tap Homebrew/bundle
brew bundle
```

## Quick Start

```bash
# clone repo
git clone git@github.com:account/repo.git
cd repo

# run setup script
bin/setup

# configure ENV variables in .env
vim .env

# run server on 5000 port
bin/server
```

## Scripts

* `bin/setup` - setup required gems and migrate db if needed
* `bin/quality` - run brakeman and rails_best_practices for the app
* `bin/ci` - should be used in the CI to run specs

## Staging

* http://hongthanhhotel-staging.herokuapp.com

## Production

* http://hongthanhhotel-production.herokuapp.com

##Deployment

###Heroku

Out of the box Rails Base ready to be deployed to Heroku.com.

* [Heroku Postgres](https://www.heroku.com/postgres) add-on will be used for database.
* [SendGrid](https://devcenter.heroku.com/articles/sendgrid#ruby-rails) add-on required to be able to send emails.
* [NewRelic](https://devcenter.heroku.com/articles/newrelic#ruby-installation-and-configuration) add-on could be used to monitor application performance.
* [Rollbar](https://elements.heroku.com/addons/rollbar) add-on could be used to application errors.

```bash
heroku create --addons=heroku-postgresql,sendgrid,newrelic,rollbar --remote staging hongthanhhotel
heroku config:add HOST="hongthanhhotel.herokuapp.com" MAILER_SENDER_ADDRESS="noreply@hongthanhhotel.herokuapp.com" NEW_RELIC_APP_NAME="hongthanhhotel"
git push staging master
heroku run rake db:schema:load
heroku open
```
