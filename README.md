# heroku-buildpacks-git-sha
Exports the Heroku SOURCE_VERSION variable (usually the Git SHA) to an env variable that
application code can access.

## Usage
To use this buildpack, the app should already be successfully running the [multi buildpack](https://github.com/heroku/heroku-buildpack-multi).

Then just add this buildpack in addition to the existing buildpacks in the `.buildpacks` file:

	https://github.com/dive-networks/heroku-buildpack-git-sha.git

The git sha will be available to application code via the env var `GIT_SHA`.

## License
MIT
