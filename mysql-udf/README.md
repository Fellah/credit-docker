# Build MySQL UDF function `udf_median.so`

Function will be builded to the `udf_median.so` library during current Docker image build.

```
$ docker build -t credit-mysql-udf .
```

After success build you could copy `udf_median.so` file from the image.

```
$ id=$(docker create credit-mysql-udf)
$ docker cp /$id:/opt/mysql-udf/udf_median.so ../mysql
$ docker rm -v $id
```
