# Credit.BY PHP Image Container Image

## Build

To build container image use standard build command in current directory.

```
$ docker build -t credit-php .
```

You could specify build tag for image.

```
$ docker build -t credit-php:5.6-apache .
```

## Run

```
$ docker run -v /php/code:/var/www/html -p 80:80 --name php credit-php
```
