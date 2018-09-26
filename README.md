# Magento 1.9.X Local Docker Environment

## Purpose
The Magedocker environment is intended to be a local environment for Magento 1.X that simulates
the most common LAMP + Redis stack that is used for Magento 1.X.

## Minimum Requirements

### Windows
* Docker 1.13

### Mac
* Docker for Mac

### Linux
* Docker

## Running the Docker Environment
From the repo root:

### Magento Configuration Settings
You can copy and paste the Magento settings for docker into app/etc/local.xml and modify them if you need.

```bash
cp docker/local.docker.xml app/etc/local.xml
```

### Brining up the environment

From this directory, with Docker already installed, all you have to do is run

```bash
docker-compose -p YOUR_PROJECT_NAME up 
```

Then add the following line to your hosts file: `127.0.0.1 YOUR_HOST_NAME.test`

You should then be able to view the following in your browser:

* `http://YOUR_HOST_NAME.test`
* `http://YOUR_HOST_NAME.test/admin`
