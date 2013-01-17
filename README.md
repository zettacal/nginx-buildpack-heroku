## ZettaCal Nginx Buildpack for Heroku

**Buildpack dependencies:**
  * Vulcan gem
  * Vulcan build server on Heroku
  * s3cmd _(for Vulcan build output S3 upload)_

**App dependencies:** 
  * Heroku config var for BUILDPACK_URL
  * `nginx.conf.erb` in application root _(Triggers buildpack and configures Nginx)_
  * Nginx buildpack in S3 bucket _(Built by Vulcan build server)_

**Usage:**

  1. Use Vulcan to build Nginx in Heroku environment & PUT resulting buildpack on S3
  1. Push the app to Heroku
