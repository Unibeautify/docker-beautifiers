# Docker Beautifiers

> Docker images for code beautifiers/formatters

## Installation

[Docker](https://docs.docker.com/engine/installation/) is required.

### Using Whalebrew

1. Install [Whalebrew](https://github.com/bfirsh/whalebrew)
2. `whalebrew install unibeautify/BEAUTIFIER`
    e.g. `whalebrew install unibeautify/php-cs-fixer`
3. Profit! You can now run the installed beautifier command.
    e.g. `php-cs-fixer --version`

### Manually

1. Pull the Docker image: `docker pull unibeautify/BEAUTIFIER`
    e.g. `docker pull unibeautify/php-cs-fixer`
2. Run the Docker image: `docker run -it -v "$(pwd)":/workdir -w /workdir unibeautify/BEAUTIFIER "--version"`
    e.g. `docker run -it -v "$(pwd)":/workdir -w /workdir unibeautify/php-cs-fixer "--version"`
