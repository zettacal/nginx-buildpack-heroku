## ZettaCal Nginx Buildpack for Heroku

**Our buildpack dependencies:**
  * Verfied Heroku account _(If not, Cloudant addon won't install)_
  * Vulcan gem _(installs Cloudant plugin with verified Heroku account)_
  * Vulcan build server on Heroku _(requires cloudant addon)_
  * s3cmd _(upload Vulcan build to S3 - in build/build_nginx:25)_
  * On S3, make sure the packaged nginx has `Content-Type: application/x-gzip`

**Our app dependencies:** 
  * Heroku config var for BUILDPACK_URL
  * `nginx.conf.erb` in application root _(Triggers buildpack)_
  * Nginx buildpack in S3 bucket _()_

**Usage:**

  1. Run the build script
  1. Push the app to Heroku
  1. Profit
