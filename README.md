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

    https://s3.amazonaws.com/foo/bar/baz.tar.gz
    https://s3.amazonaws.com/foo/bar/qux.tar.gz
    ...

Binaries
========

Binaries are cached and extracted to the **/app/bin** directory. 
They should be gzipped tarbells containing a single binary.

