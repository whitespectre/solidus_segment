Solidus Segment
==============

Provides support for [Segment](https://segment.com/docs/spec/) APIs: 
* Indentify (Ruby)
* Track ecommerce events 
    *  Cart Viewed (Js)
    *  Checkout Started (Js)
    *  Checkout Step Viewed (Js)
    *  CompleteRegistration FB (Ruby)
    *  Order Completed (Ruby)
    *  Product Added (Ruby)
    *  Product Clicked (Ruby)    
    *  Payment Info Entered (Js)
    *  Product List Filtered (Js)
    *  Product List Viewed (Js)
    *  Product Removed (Js)
    *  Product Viewed (Js)
    *  Products Searched (Js)
    *  Sign In User (Ruby)
* Page with the segment [analytics.js](https://segment.com/docs/sources/website/analytics.js/quickstart/) 

We combine [Javascript Source](https://segment.com/docs/sources/website/analytics.js/) and [Ruby Source](https://segment.com/docs/sources/server/ruby/) for the server-side library

Some of the ideas behind are inspired by 
* https://github.com/spree-contrib/spree_analytics_trackers
* https://www.cookieshq.co.uk/posts/how-we-use-segment-with-solidus-spree
* https://robots.thoughtbot.com/segment-io-and-ruby


Installation
------------

Add solidus_segment to your Gemfile:

```ruby
gem 'solidus_segment', github: '2beDigital/solidus_segment'
```

Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g solidus_segment:install
```

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs, and [Rubocop](https://github.com/bbatsov/rubocop) static code analysis. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'solidus_segment/factories'
```

TODO
-------
Some additional events and features could include:
* Promotions 
* Order updated , order cancelled, order refunded
* Coupons, sharing, Wishlisting , reviewing
* Avoid class_eval improve the code
* Test coverage


Copyright (c) 2019 [2beDigital](http://www.2bedigital.com/?utm_source=github), released under the New BSD License



