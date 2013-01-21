## ZettaCal Nginx Buildpack for Heroku

**Our buildpack dependencies:**
  * Verfied Heroku account _(If not, Cloudant addon may not install)_
  * Vulcan gem
  * Vulcan build server _(requires Cloudant)_
  * s3cmd utility

**Our app dependencies:** 
  * This buildpack on github
  * Heroku config var for BUILDPACK_URL
  * Nginx package in S3 bucket
  * Presense of build/index.html _(Triggers buildpack)_

**Usage:**

  1. Run the build script
  1. Push the buildpack to Github
  1. Deploy the app to Heroku
  1. Profit
