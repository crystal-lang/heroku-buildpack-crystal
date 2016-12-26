# Crystal Heroku Buildpack

You can create an app in Heroku with Crystal's buildpack by running the
following command:

```bash
$ heroku create myapp --buildpack https://github.com/crystal-lang/heroku-buildpack-crystal.git
```

The default behaviour is to use the [latest crystal release](https://github.com/crystal-lang/crystal/releases/latest).
If you need to use a specific version create a `.crystal-version` file in your
application root directory with the version that should be used (e.g. `0.17.1`).

## Requirements

In order for the buildpack to work properly you should have a `shard.yml` file,
as it is how it will detect that your app is a Crystal app.

Your application has to listen on a port defined by Heroku. It is given to you
through the command line option `--port` and the environment variable `PORT`
(accessible through `ENV["PORT"]` in Crystal). However, most web frameworks
should handle this for you.

## Testing

To test a change to this buildpack, write a unit test in `tests/run` that asserts your change and
run `make test` to ensure the change works as intended and does not break backwards compatibility.

## More info

To learn more about how to deploy a Crystal application to Heroku, read
[our blog post](http://crystal-lang.org/2016/05/26/heroku-buildpack.html).

## Older versions of Crystal

If you have and older version of Crystal (`<= 0.9`), that uses the old
`Projectfile` way of handling dependencies, please upgrade :-).
