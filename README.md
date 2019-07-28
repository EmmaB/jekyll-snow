# Snowbooks website

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

## Generate credentials on Consonance (General Products developers only)

`ApiKey.create(client: Client.is_snowbooks).key`

## How to run

* Add and remove products to be included on the site, on Consonance:

`https://web.consonance.com/shops/:id/products`

On the command line:

`API_KEY=1234567890 ruby lib/seed.rb`

`jekyll build --watch`

To run the site locally:

`jekyll serve`


~~To push to production:~~

~~* Build for production~~

~~`JEKYLL_ENV=production jekyll build`~~

~~Push to S3 AWS account emma+snow~~

~~We use `https://github.com/laurilehmijoki/s3_website`~~

~~`s3_website push`~~

~~It will calculate the diff, update the changed files, upload the new files and delete the obsolete files.~~

Now hosted on Netlify. Push master to git origin to deploy via an automatic pipeline. No need to build before pushing as Netlify uses deploy hooks to run `jekyll build`. 

[![Netlify Status](https://api.netlify.com/api/v1/badges/f9528ec6-7dd5-467d-ac49-300a916e97cb/deploy-status)](https://app.netlify.com/sites/snowbooks/deploys)

## TODO

[x] google analytics

[x] more shop links

[x] refine list on consonance of what should be published

[x] set up aws

[x] schema.org

[x] blog

[x] home page copy
