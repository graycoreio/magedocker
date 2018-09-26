# Magento 1.9.X Local Docker Environment

## Purpose

## Minimum Requirements

### Windows
* Docker 1.13

### Mac
* Docker for Mac

### Linux

## Running the Docker Environment
From the repo root:

```bash
cp docker/local.docker.xml app/etc/local.xml
```

From this directory, with Docker already installed, all you have to do is run

```bash
docker-compose -p YOUR_PROJECT_NAME up 
```

Then add the following line to your hosts file: `127.0.0.1 YOUR_HOST_NAME.test`

You should then be able to view the following in your browser:

* `http://YOUR_HOST_NAME.test`
* `http://YOUR_HOST_NAME.test/ADMIN_URL`
