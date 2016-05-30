# Crystal Heroku Buildpack

You can create an app in Heroku with Crystal's buildpack by running the
following command:

```bash
$ heroku create myapp --buildpack https://github.com/crystal-lang/heroku-buildpack-crystal.git
```

In order for the buildpack to work properly you should have a `shard.yml`
file, as it is how it will detect that your app is a Crystal app.

The default behaviour is to use the [latest crystal
release](https://github.com/crystal-lang/crystal/releases/latest). If you need
to use a specific version create a `.crystal-version` file in your application
root directory with the version that should be used (e.g. `0.17.1`).

To learn more about how to deploy a Crystal application to Heroku, read [our
blog post](http://crystal-lang.org/2016/05/26/heroku-buildpack.html).

HTTP port comes from command line option `--port` or from `ENV["PORT"]`.

## Older versions of Crystal

If you have and older version of Crystal (`<= 0.9`), that uses the old
`Projectfile` way of handling dependencies, please upgrade :-).
