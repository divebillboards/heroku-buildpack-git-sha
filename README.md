# OBSOLETE

This repository is obsolete. See:

https://github.com/dive-networks/dive-web-app/commit/1ce574f31a4624e279b2e0f101261900271f5456

# heroku-buildpacks-git-sha

Exports the Heroku SOURCE_VERSION variable (usually the Git SHA) to an env variable that
application code can access.

## Usage
The first step is to add the Heroku [multi buildpack](https://github.com/heroku/heroku-buildpack-multi) to your app.
Next, create a `.buildpacks` file in your app repo or edit an existing file. Add this to the file:

	https://github.com/dive-networks/heroku-buildpack-git-sha.git

The Git sha will now be available to application code via the env var `GIT_SHA`.

## License
MIT
