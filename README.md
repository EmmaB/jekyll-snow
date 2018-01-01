# Snowbooks

## Develop

This app was built with [Jekyll](http://jekyllrb.com/) version 3.3.1, but should support newer versions as well.

Install the dependencies with [Bundler](http://bundler.io/):

~~~bash
$ bundle install
~~~

Run `jekyll` commands through Bundler to ensure you're using the right versions:

~~~bash
$ bundle exec jekyll serve
~~~

## Set up API to Bibliocloud

This is a one-off, but nevertheless:

`ApiKey.create(client: Client.is_snowbooks).key`

## How to run

* Add and remove products to be included on the site on Bibliocloud:
https://app.bibliocloud.com/shops/1/products

On the command line:

* ruby lib/seed.rb
* jekyll build --watch

To run the site locally:
* jekyll serve

We use https://github.com/laurilehmijoki/s3_website
To push to S3:

* s3_website push

It will calculate the difference, update the changed files, upload the new files and delete the obsolete files.

TODO

[x] google analytics
[x] more shop links
[x] refine list on bibliocloud of what should be published
[x] set up aws
[ ] search
[x] schema.org
[ ] blog?
[x] home page copy
[ ] tests
