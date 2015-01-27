# NGINX Buildpack for Dokku - Serving static rails assets
This buildpack has been successfully run on Digital Ocean instances of Ubuntu 14.04 (Status: Jan 2015). It might also work with different configurations.

## Purpose
`buildpack-rails-assets` provides a simple, low overhead way of serving static rails assets on Dokku. 

## Usage
1. `dokku config:set <APPLICATION> BUILDPACK_URL=https://github.com/MichaelSp/buildpack-rails-assets.git`
2. Push your project to Dokku

All static files that you want to serve should be in the public directory of your repository. `buildpack-rails-assets` will automatically download the buildpack, download NGINX, compile it, and install it. The next time you push your project, the buildpack will reuse the precompiled binaries. 

## Credits and License
`buildpack-rails-assets` is licensed under the CC0 1.0 Universal license and has been informed by many similar projects on the web

