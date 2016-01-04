FROM ubuntu

RUN apt-get update -y
RUN apt-get install -y g++ libmysql++-dev

ADD https://github.com/megastep/mysql-udf/archive/master.tar.gz /tmp/mysql-udf.tar.gz

RUN mkdir /opt/mysql-udf
RUN tar -zxf /tmp/mysql-udf.tar.gz -C /opt/mysql-udf --strip-components 1

WORKDIR /opt/mysql-udf

RUN gcc -fPIC -shared -lstdc++ -I /usr/include/mysql -I /usr/local/include -I /usr/local/mysql/include/ -o udf_median.so udf_median.cc
