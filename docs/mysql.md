# MySQL Container

## Purpose
The magedocker environment includes a MySQL 5.7 container that has a volume mount for persistence. If you're familiar with docker volumes and containers, then the following workflows should be familiar.

You can read more about the specifics of configuring the container [here](https://hub.docker.com/_/mysql/).

## Table of Contents
* [Seeding Data](#seeding-data)
* [Getting New Data In](#getting-new-data-in)
* [Getting Data Out](#getting-data-out)

### Seeding Data
Seeding the container with data is pretty easy. The MySQL container will import any `.sql` or `.sql.gz` file located in `magedocker/docker-entrypoint-initdb.d` into the configured "default" MySQL database.

### Getting New Data In
If you'd like to UPDATE your database with some additional data, you can import into the running MySQL container fairly easily.

```
docker exec YOUR_PROJECT_NAME_mysql_1 mysql -u magento -p magento < your_sql.sql
```

### Getting Data Out
If you need to get data out of the running MySQL container you can also do so fairly easily.

```
docker exec YOUR_PROJECT_NAME_mysql_1 mysqldump -u magento -p magento > dump.sql
```

> This does NOT work on Windows. There are encoding issues between Linux and Windows. You will need to run a slightly different command in powershell.

```
docker exec YOUR_PROJECT_NAME_mysql_1 mysqldump -u magento --password=magento magento | Set-Content backup.sql
```