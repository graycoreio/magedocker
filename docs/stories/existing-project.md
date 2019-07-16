# Working with an Existing Magento 1.X Project

Getting a Magento 1.X project running in Magedocker is fast and easy. It requires familiarity with the command line (or terminal), and basic familarity with docker and git.

## Cloning the project
From the root of your Magento project, we'll need to clone down the Magedocker project.

```bash
cd /path/to/my/magento/project
git clone https://github.com/graycoreio/magedocker && cd magedocker
```

## Configuring the project
In the root of the magedocker folder, you'll find a `.env.sample` file. Replace `YOUR_PROJECT_NAME` with the name of your project on this line:

```txt
COMPOSE_PROJECT_NAME=YOUR_PROJECT_NAME
```

## Start the environment
From the root of the Magedocker directory, we will now use `docker-compose` to bring up the project.

```bash
docker-compose up
```

## Bring down the environment
We can stop the environment by running:

```bash
docker-compose down
```

### Other useful stories
* [Importing a custom database](./working-with-mysql.md)
* [Switching PHP versions](./php-switching.md)