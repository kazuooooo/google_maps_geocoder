# GoogleMapsGeocoder

[![Build Status](https://secure.travis-ci.org/ivanoblomov/google_maps_geocoder.png)](http://travis-ci.org/ivanoblomov/google_maps_geocoder)
[![Code Climate](https://codeclimate.com/github/ivanoblomov/google_maps_geocoder.png)](https://codeclimate.com/github/ivanoblomov/google_maps_geocoder)
[![Coverage Status](https://coveralls.io/repos/ivanoblomov/google_maps_geocoder/badge.svg?branch=master&service=github)](https://coveralls.io/github/ivanoblomov/google_maps_geocoder?branch=master)
[![Dependency Status](https://gemnasium.com/ivanoblomov/google_maps_geocoder.png)](https://gemnasium.com/ivanoblomov/google_maps_geocoder)
[![Inch CI](https://inch-ci.org/github/Ivanoblomov/google_maps_geocoder.svg?branch=master&amp;style=flat)](https://inch-ci.org/github/Ivanoblomov/google_maps_geocoder)
[![Gem Version](https://badge.fury.io/rb/google_maps_geocoder.svg)](http://badge.fury.io/rb/google_maps_geocoder)

A simple Plain Old Ruby Object wrapper for geocoding with Google Maps.

## Installation

Add GoogleMapsGeocoder to your Gemfile and run `bundle`:

```ruby
  gem 'google_maps_geocoder'
```

Or try it out in `irb` with:

```ruby
  require './lib/google_maps_geocoder/google_maps_geocoder'
```

## Ready to Go in One Step

```ruby
chez_barack = GoogleMapsGeocoder.new '1600 Pennsylvania Washington'
```

## Usage

Get the complete, formatted address:

```ruby
chez_barack.formatted_address
 => "1600 Pennsylvania Avenue Northwest, President's Park, Washington, DC 20500, USA"
```

...standardized name of the city:

```ruby
chez_barack.city
 => "Washington"
```

...full name of the state or region:

```ruby
chez_barack.state_long_name
 => "District of Columbia"
```

...standard abbreviation for the state/region:

```ruby
chez_barack.state_short_name
 => "DC"
```

## API

The complete, hopefully self-explanatory, API is:

* `GoogleMapsGeocoder#city`
* `GoogleMapsGeocoder#country_long_name`
* `GoogleMapsGeocoder#country_short_name`
* `GoogleMapsGeocoder#county`
* `GoogleMapsGeocoder#exact_match?`
* `GoogleMapsGeocoder#formatted_address`
* `GoogleMapsGeocoder#formatted_street_address`
* `GoogleMapsGeocoder#lat`
* `GoogleMapsGeocoder#lng`
* `GoogleMapsGeocoder#partial_match?`
* `GoogleMapsGeocoder#postal_code`
* `GoogleMapsGeocoder#state_long_name`
* `GoogleMapsGeocoder#state_short_name`

## Google Maps API Key (Optional)

To have GoogleMapsGeocoder use your Google Maps API key, set it as an environment variable:

```bash
export GOOGLE_MAPS_API_KEY=[your key]
```

## Contributing to google_maps_geocoder

* Check out the latest master to make sure the feature hasn't been implemented or the bug hasn't been fixed yet
* Check out the issue tracker to make sure someone already hasn't requested it and/or contributed it
* Fork the project
* Start a feature/bugfix branch
* Commit and push until you are happy with your contribution
* Make sure to add tests for it. This is important so I don't break it in a future version unintentionally.
* Please try not to mess with the Rakefile, version, or history. If you want to have your own version, or is otherwise necessary, that is fine, but please isolate to its own commit so I can cherry-pick around it.

## Copyright

Copyright (c) 2011 Roderick Monje. See LICENSE.txt for further details.
