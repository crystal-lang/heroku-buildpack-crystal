# Crystal Heroku Buildpack

You can create an app in Heroku with Crystal's buildpack by running the
following command:

```bash
$ heroku create myapp --buildpack https://github.com/zamith/heroku-buildpack-crystal.git
```

In order for the buildpack to work properly you should have a `shard.yml`
file, as it is how it will detect that your app is a Crystal app.

To learn more about using custom buildpacks in Heroku, read [their docs](https://devcenter.heroku.com/articles/third-party-buildpacks#using-a-custom-buildpack).
