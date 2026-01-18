# WordPress with Docker Compose

This project provides a local WordPress environment with a MySQL database using Docker Compose.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Quickstart](#quickstart)
3. [Usage](#usage)

## Prerequisites

- Docker
- Docker Compose
- Git

## Quickstart

1. Clone the repository

```bash
git clone https://github.com/MarcoLenschau/Wordpress-Container 
```

2. Change Directory

```bash
cd Wordpress-Container
```

3. Create .env file

```bash
mv example.env production.env
```

> [!IMPORTANT]
> Open `production.env` and enter your own values for the database credentials

4. Start the Container

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

### Useful Commands

- Start containers: `docker-compose up -d`
- Stop containers: `docker-compose down`
- Show logs: `docker-compose logs wordpress`

### Troubleshooting

- Check environment variables and credentials
- Check if the database is running: `docker-compose ps`
- Check logs for error messagessss