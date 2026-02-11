# Dev Container Environment Setup.

This setup is designed to allow experimenting with Ubuntu LTS sandbox testing.

## Setup Requirements

Note: Other IDEs can support this devcontainer setup in the future.

### Base Requirements:

* [Docker](https://www.docker.com/)

### For VS Code:

* [VS Code](https://code.visualstudio.com/download)
  * [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Features

* A mounted project directory so you can access project files.
* Experiment without your local being affected.
* Reset fast like you just started from a fresh install.
* Access your project experiment result files locally.

## Notes

* Custom password setup security requirement is low since its only used in a dev container for experimentation.
* You can choose to avoid sudo user password prompt by uncommenting one line in [Dockerfile](./.devcontainer/Dockerfile).
* Devcontainer will create an `out` directory which will contain your project files before starting.
