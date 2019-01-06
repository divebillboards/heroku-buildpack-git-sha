# heroku-buildpacks-git-sha

Exports the Heroku `SOURCE_VERSION` variable (usually the Git `SHA`) to an
environment variable as `GIT_SHA` that application code can access at runtime.


## Usage

This buildpack must be used in concert with one or more others. Heroku supports
[multiple buildpacks](https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app#adding-a-buildpack)
out of the box.

The order of buildpacks does matter. You probably want this one first in the
order. For example:

```bash
heroku buildpacks:add --index 1 https://github.com/dive-networks/heroku-buildpack-git-sha.git
```


The Git `SHA` will now be available to application code via `GIT_SHA`. Examples:

```
Node    process.env['GIT_SHA']
Java    System.getenv("GIT_SHA")
Scala   sys.env("GIT_SHA")
```


## License

MIT
