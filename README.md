#  Dockerized PHP 7 Application

---

## Overview
This project is a Dockerized **PHP 7** environment with **NGINX**, **MySQL**, and **phpMyAdmin**.

---

## Services
- **PHP**: Runs the PHP application.
- **NGINX**: Serves as the web server.
- **MySQL**: Database for your application.
- **phpMyAdmin**: Database management UI.

---

## Setup Instructions

1. **Set Up Environment Variables**:
   - Create a `.env` file in the root directory:
     ```bash
     cp .env.example .env
     ```

2. **Build and Start Containers**:
   ```bash
   docker-compose up -d --build
   ```

3. **Access Services**:
   - Application: [http://localhost:8000](http://localhost:8000)
   - phpMyAdmin: [http://localhost:8080](http://localhost:8080)

---

## Project Structure
- `public/`: PHP source code.
- `docker/nginx/`: nginx configuration files.
- `docker/php/`: PHP Dockerfile and settings.
- `docker/mysql/`: MySQL configuration files.

---

## Commands
- Start the project:
  ```bash
  docker-compose up -d
  ```
- Stop the project:
  ```bash
  docker-compose down -v
  ```
---

