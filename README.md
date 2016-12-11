# Hồng Thanh Hotel Management System

Third-party service badges (if available)

[![Build Status](https://semaphoreci.com/api/v1/khuonglh/hongthanhhotel/branches/master/badge.svg)](https://semaphoreci.com/khuonglh/hongthanhhotel)
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
