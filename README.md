Heroku buildpack: Bin Urls
-------------------------

A [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for deploying binaries via urls.
You should use [heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi) in order to use this with other buildpacks.

Usage
=====

/app/.buildpacks:

    https://github.com/psirenny/heroku-buildpack-bin-urls.git
    https://github.com/heroku/heroku-buildpack-nodejs.git
    ...

/app/.binurls:

    https://s3.amazonaws.com/blrrt/bin/ffmpeg.tar.gz
    https://s3.amazonaws.com/blrrt/bin/ffprobe.tar.gz
    ...

Binaries
========

Binaries are placed in the **/app/bin** directory.

Urls
====

Binary urls should be gzipped tarballs. They are cached between installs.
