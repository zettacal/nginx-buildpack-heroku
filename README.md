# ZettaCal Nginx Buildpack for Heroku

**Buildpack dependencies:**
  * Vulcan gem
  * Vulcan build server on Heroku

**App dependencies:** 
  * `nginx.conf.erb` in application root _(set in Buildpack bin/detect & used to configure Nginx)_
  * Our Nginx build staged in our S3 bucket (Built by Vulcan build server)
  * Heroku config var for BUILDPACK_URL

**Usage:**

  1. Run Vulcan server to build Nginx in Heroku environment
  1. Put Vulcan output where the Buildpack expects it _(bin/compile:34)_
  1. Push the app to Heroku

**Versions:** _(build/build_nginx)_
  * Nginx v1.2.6
  * PCRE v8.32
