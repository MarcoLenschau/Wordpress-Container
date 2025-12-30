# WordPress with Docker Compose

## Table of Contents

1. [Overview](#overview)
2. [Requirements](#requirements)
3. [Installation & Startup](#installation--startup)
4. [Environment Variables](#environment-variables)
5. [Checking Database Connection](#checking-database-connection)
6. [Useful Commands](#useful-commands)
7. [Troubleshooting](#troubleshooting)

## Overview

This project provides a local WordPress environment with a MySQL database using Docker Compose.

## Requirements

- Docker
- Docker Compose

## Installation & Startup

```bash
docker-compose up -d
```

Afterwards, WordPress is available at [http://localhost:8080](http://localhost:8080).

## Environment Variables

The most important variables are set in the `.env` files:

- WORDPRESS_DB_HOST
- WORDPRESS_DB_USER
- WORDPRESS_DB_PASSWORD
- WORDPRESS_DB_NAME
- MYSQL_DATABASE
- MYSQL_USER
- MYSQL_PASSWORD
- MYSQL_RANDOM_ROOT_PASSWORD

## Checking Database Connection

- In the browser: If the connection is successful, WordPress loads normally. If there are problems, you will see "Error establishing a database connection".
- In the terminal: Check logs with
  ```bash
  docker-compose logs wordpress
  ```
- In the backend: Is login to the WordPress admin area possible?

## Useful Commands

- Start containers: `docker-compose up -d`
- Stop containers: `docker-compose down`
- Show logs: `docker-compose logs wordpress`

## Troubleshooting

- Check environment variables and credentials
- Check if the database is running: `docker-compose ps`
- Check logs for error messages