## ZettaCal Nginx Buildpack for Heroku

**Our buildpack dependencies:**
  * Verfied Heroku account _(If not, Cloudant addon won't install)_
  * Vulcan gem
  * Vulcan build server _(requires Cloudant addon)_
  * s3cmd utility
  * `Content-Type: application/x-gzip` on packaged nginx .tgz

**Our app dependencies:** 
  * This buildpack on github
  * Heroku config var for BUILDPACK_URL
  * Nginx package in S3 bucket _(Our build script puts it there)_
  * Presense of build/index.html _(Triggers buildpack)_
  * Properly configured nginx

**Usage:**

  1. Run the build script
  1. Push the buildpack to Github
  1. Push the app to Heroku
  1. Profit
