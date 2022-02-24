# Mysql with Docker Compose

This is a basic WAMP stack environment built using Docker Compose. It consists following:

* MySQL v8
* phpMyAdmin

## Installation

Clone this repository on your local computer. Run the `docker-compose up`.

```shell
git clone https://github.com/german1311/docker-compose-mysql
cd docker-compose-wamp/
git fetch --all
docker-compose up
```

Your phpMyAdmin stack is now ready!! You can access it via `http://localhost:8080`.

## Configuration

This package comes with default configuration options. You can modify them by creating `.env` file in your root directory.

To make it easy, just copy the content from `sample.env` file and update the environment variable values as per your need.

### Configuration Variables

There are following configuration variables available and you can customize them by overwritting in your own `.env` file.


_**MYSQL_DATA_DIR**_

This is MySQL data directory. The default value for this is `./data/mysql`. All your MySQL data files will be stored here.

_**MYSQL_LOG_DIR**_

This will be used to store Apache logs. The default value for this is `./logs/mysql`.

#### Connect via SSH

You can connect to web server using `docker exec` command to perform various operation on it. Use below command to login to container via ssh.

```shell
docker exec -it mysql /bin/bash
```

## phpMyAdmin

phpMyAdmin is configured to run on port 8080. Use following default credentials.

http://localhost:8080/  
username: root  
password: tiger
