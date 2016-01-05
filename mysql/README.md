# Credit.BY MySQL Container Image

## Build

To build container image use standard build command in current directory.

```
$ docke build -t credit-mysql .
```

## Configure

At first we should run container to setup MySQL. For more details please read description for the [official MySQL container image](https://hub.docker.com/_/mysql/).

```
$ docker run -v /mysql/data:/var/lib/mysql --env-file env.list --rm --name mysql credit-mysql
```

In the `env.list` file you could find environment variables to configure base credentials to access MySQL.

For project we need additional function. You should create it using command below.

```
$ docker exec -it mysql mysql -u root -p -e "CREATE AGGREGATE FUNCTION median RETURNS REAL SONAME 'udf_median.so';"
```

After that we could stop container.

```
$ docker stop mysql
```

Now MySQL data directory could be copied to the server. We have finished base configuration.

## Run

To run container you could use simple command below.

```
$ docker run -v /mysql/data:/var/lib/mysql --rm --name mysql credit-mysql
```
