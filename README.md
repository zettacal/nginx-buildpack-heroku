# ZettaCal Nginx Buildpack for Heroku

**Buildpack dependencies:**
  * Vulcan gem
  * Vulcan build server on Heroku with config var for BUILDPACK_URL

**App dependencies:** 
  * `nginx.conf.erb` in application root _(set in Buildpack bin/detect & used to configure Nginx)_
  * Our Nginx build staged in our S3 bucket (Built by Vulcan build server)
  * Heroku config var for BUILDPACK_URL

**Usage:**

  1. Upon ???, our Heroku Vulcan build server compiles Nginx and PUTs it in our S3 bucket
  1. Upon git push, our Heroku Cedar app GETs this buildpack from our S3 bucket

**Versions:** _(set in build/build_nginx)_
  * Nginx v1.2.6
  * PCRE v8.32
