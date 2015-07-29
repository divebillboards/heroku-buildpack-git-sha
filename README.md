# heroku-buildpacks-git-sha

Writes the SOURCE_VERSION variable (usually the Git SHA) to a file for use by the app.

## Usage

To use this buildpack, the app should already be successfully running the [multi buildpack](https://github.com/heroku/heroku-buildpack-multi).

Then just add this buildpack in addition to the existing buildpacks in the `.buildpacks` file:

	https://github.com/dive-networks/heroku-buildpack-git-sha.git

In the application code, read the `.source_version` file that will be created on deployment.
Add any error handling for environments where this file doesn't exist, such as your development machine.

## License
MIT
