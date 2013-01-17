# ZettaCal Nginx Buildpack for Heroku

**Buildpack dependency:**
  * Vulcan gem
  * Vulcan build server on Heroku
  * Heroku config var for BUILDPACK_URL

**App dependency:** 
  * `nginx.conf.erb` in application root _(set in bin/detect & used to configure Nginx)_
  * Our Nginx build staged in our S3 bucket (Built by Vulcan build server)
  * Heroku config vars for AWS_ID, AWS_SECRET, S3_BUCKET

**Usage:**

  1. Upon ???, our Heroku Vulcan build server compiles Nginx and PUTs it in our S3 bucket
  1. Upon git push, our Heroku Cedar app GETs this buildpack from our S3 bucket

**Versions:** _(set in build/package_nginx)_
  * Nginx v1.2.6
  * PCRE v8.32
