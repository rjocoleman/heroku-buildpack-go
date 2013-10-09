# Heroku Buildpack: Go

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for [Go](http://golang.org/).
It installs and adds the Go binary to your `$PATH`.

Useful with [https://github.com/ddollar/heroku-buildpack-multi](https://github.com/ddollar/heroku-buildpack-multi)

Based on [https://github.com/kr/heroku-buildpack-go](https://github.com/kr/heroku-buildpack-go)

## Example

```
$ heroku create -b https://github.com/rjocoleman/heroku-buildpack-go.git
...

$ git push heroku master
...
-----> Fetching custom git buildpack... done
-----> Go app detected
-----> Installing Go 1.1.2... done
-----> Discovering process types
       Procfile declares types -> web
-----> Compiled slug size: 1.0MB
-----> Launching... done, v5
       http://pure-sunrise-3607.herokuapp.com deployed to Heroku
```

## Hacking on this Buildpack

To change this buildpack, fork it on GitHub. Push
changes to your fork, then create a test app with
`--buildpack YOUR_GITHUB_GIT_URL` and push to it. If you
already have an existing app you may use `heroku config:add
BUILDPACK_URL=YOUR_GITHUB_GIT_URL` instead of `--buildpack`.

[go]: http://golang.org/
[buildpack]: http://devcenter.heroku.com/articles/buildpacks
