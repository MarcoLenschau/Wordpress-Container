# WordPress with Docker Compose

This project provides a local WordPress environment with a MySQL database using Docker Compose.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Quickstart](#quickstart)
3. [Usage](#usage)

## Prerequisites

- Docker
- Docker Compose

## Quickstart

```bash
git clone https://github.com/MarcoLenschau/Wordpress-Container 
```

### Change Directory

```bash
cd Wordpress-Container
```

### Create .env file

```bash
mv example.env production.env
```

**Important:** After renaming the file:
1. Open `production.env` and enter your own values for the database credentials

### Start the Container

```bash
docker-compose up -d
```

### How to access the App

Afterwards, WordPress is available at http://<your_ip>/8080.

## Usage

### Environment Variables

The most important variables are set in the `.env` files:

- WORDPRESS_DB_HOST
- WORDPRESS_DB_USER
- WORDPRESS_DB_PASSWORD
- WORDPRESS_DB_NAME
- MYSQL_DATABASE
- MYSQL_USER
- MYSQL_PASSWORD
- MYSQL_RANDOM_ROOT_PASSWORD

### Checking Database Connection

- In the browser: If the connection is successful, WordPress loads normally. If there are problems, you will see "Error establishing a database connection".
- In the terminal: Check logs with
  ```bash
  docker-compose logs wordpress
  ```
- In the backend: Is login to the WordPress admin area possible?

### Useful Commands

- Start containers: `docker-compose up -d`
- Stop containers: `docker-compose down`
- Show logs: `docker-compose logs wordpress`

### Troubleshooting

- Check environment variables and credentials
- Check if the database is running: `docker-compose ps`
- Check logs for error messagessss