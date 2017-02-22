# Awesome Dockerized PHP tools

> A curated list of amazingly awesome Dockerized PHP tools.

These Docker images fulfil the following requirements:

* The Docker image must be availabe via Docker Hub
* The Dockerfile source must be available (on Github, Bitbucket, ...)
* The Docker image do support the current version of the contained PHP tool
* (The Docker image are based on Alpine Linux for minimimal filesize usage)

---

### Codeception

Codeception is a modern full-stack testing framework for PHP.

| [Project](http://codeception.com/) | [Docker Hub](https://hub.docker.com/r/codeception/codeception/) | [Dockerfile Repository](https://github.com/Codeception/Codeception)
| ------------- | ------------- | ------------- |

Usage:

```
docker run -v ${PWD}:/project codeception/codeception run
```

### Composer

Composer is a tool for dependency management in PHP, written in PHP.

| [Project](https://getcomposer.org/) | [Docker Hub](https://hub.docker.com/_/composer/) | [Dockerfile Repository](https://github.com/composer/docker)
| ------------- | ------------- | ------------- |

Usage:

```
docker run --rm --interactive --tty --volume $PWD:/app composer install
```

---

### Humbug

Humbug is a Mutation Testing framework for PHP to measure the real effectiveness of your test suites and assist in their improvement.

| [Project](https://github.com/padraic/humbug) | [Docker Hub](https://hub.docker.com/r/tommymuehle/docker-php-humbug/) | [Dockerfile Repository](https://github.com/tommy-muehle/docker-php-humbug)
| ------------- | ------------- | ------------- |

Usage:

```
docker run -v $PWD:/app --rm tommymuehle/docker-php-humbug
```

---

### PHPCBF

PHP_CodeSniffer's phpcbf is a script to automatically correct coding standard violations.

| [Project](https://github.com/squizlabs/PHP_CodeSniffer) | [Docker Hub](https://hub.docker.com/r/herloct/phpcbf/) | [Dockerfile Repository](https://github.com/herloct/docker-phpcbf)
| ------------- | ------------- | ------------- |

Usage:

```
docker run --rm --user $(id -u):$(id -g) -v $(pwd):/project herloct/phpcbf
```

---

### PHPCS Fixer

PHP_CodeSniffer tokenizes PHP and detects violations of a defined set of coding standards.

| [Project](https://github.com/squizlabs/PHP_CodeSniffer) | [Docker Hub](https://hub.docker.com/r/herloct/phpcs/) | [Dockerfile Repository](https://github.com/herloct/docker-phpcs)
| ------------- | ------------- | ------------- |

Usage:

```
docker run --rm -v /local/path:/project herloct/phpcs
```

---

### PHP Coding Standards Fixer

The Coding Standards fixer for your code.

| [Project](http://cs.sensiolabs.org/) | [Docker Hub](https://hub.docker.com/r/herloct/php-cs-fixer/) | [Dockerfile Repository](https://github.com/herloct/docker-php-cs-fixer)
| ------------- | ------------- | ------------- |

Usage:

```
docker run --rm --user $(id -u):$(id -g) -v /local/path:/project herloct/php-cs-fixer
```

---

### PHPStan

PHP Static Analysis Tool - discover bugs in your code without running it!

| [Project](https://github.com/phpstan/phpstan) | [Docker Hub](https://hub.docker.com/r/phpstan/phpstan/) | [Dockerfile Repository](https://github.com/phpstan/docker-image)
| ------------- | ------------- | ------------- |

Usage:

```
docker run -v $PWD:/app --rm phpstan/phpstan analyse /app/src
```

---

### PHPUnit

The PHP Unit Testing framework.

| [Project](https://phpunit.de) | [Docker Hub](https://hub.docker.com/r/phpunit/phpunit/) | [Dockerfile Repository](https://github.com/JulienBreux/phpunit-docker)
| ------------- | ------------- | ------------- |

Usage:

```
docker run -v $(pwd):/app --rm phpunit/phpunit run
```

---

### Security-Checker

Check your PHP project for known security issues!

| [Project](https://security.sensiolabs.org/) | [Docker Hub](https://hub.docker.com/r/jsixc/sensiolabs-security-checker/) | [Dockerfile Repository](https://github.com/jak/sensiolabs-security-checker-docker)
| ------------- | ------------- | ------------- |

Usage:

```
docker run --rm -v $(pwd)/composer.lock:/composer.lock jsixc/sensiolabs-security-checker:7.1
```
