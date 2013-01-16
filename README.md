# ZettaCal Nginx Buildpack for Heroku

*Buildpack dependency:*
  * Vulcan gem
  * S3 with Heroku environment constants for AWS_ID AWS_SECRET S3_BUCKET

*App dependency:* _(set in bin/detect)_
  * `nginx.conf.erb` in application root _(used to configure nginx)_

*Usage:*
1. Upon ???, our Heroku Vulcan build server compiles Nginx and PUTs it in our S3 bucket
1. Upon git push, our Heroku Cedar app GETs this buildpack from our S3 bucket

*Versions:* _(set in support/package_nginx)_
  * Nginx v1.2.6
  * PCRE v8.32
