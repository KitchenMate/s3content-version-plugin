# s3content-version-plugin

This jupyterlab plugin allows for running (but not editing) of older versions of a notebook hosted on the s3contents backend.

Note: this plugin requires a fork of s3contents w/ version control hooks.
To install this fork, add the following to your Pipfile (for pipenv users):
```toml
s3contents = {editable = true, git = "https://github.com/KitchenMate/s3contents.git", ref = "master"}
```

![Image of Dropdown](https://raw.githubusercontent.com/KitchenMate/s3content-version-plugin/master/dropdown-screenshot.png)
![Image of Prompt](https://raw.githubusercontent.com/KitchenMate/s3content-version-plugin/master/prompt-screenshot.png)

## Requirements

* JupyterLab >= 1.0
* s3contents (KitchenMate fork)
* s3 bucket with versioning turned on

## Install

```bash
jupyter labextension install s3content-version-plugin
```

## Contributing

### Install

The `jlpm` command is JupyterLab's pinned version of
[yarn](https://yarnpkg.com/) that is installed with JupyterLab. You may use
`yarn` or `npm` in lieu of `jlpm` below.

```bash
# Clone the repo to your local environment
# Move to s3content-version-plugin directory
# Install dependencies
jlpm
# Build Typescript source
jlpm build
# Link your development version of the extension with JupyterLab
jupyter labextension link .
# Rebuild Typescript source after making changes
jlpm build
# Rebuild JupyterLab after making any changes
jupyter lab build
```

You can watch the source directory and run JupyterLab in watch mode to watch for changes in the extension's source and automatically rebuild the extension and application.

```bash
# Watch the source directory in another terminal tab
jlpm watch
# Run jupyterlab in watch mode in one terminal tab
jupyter lab --watch
```

### Uninstall

```bash
jupyter labextension uninstall s3content-version-plugin
```

