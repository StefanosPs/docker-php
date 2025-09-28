## Description

This project provides a Docker-based development environment for PHP
applications. It allows developers to quickly set up and run Symfony projects
across different machines with minimal configuration, requiring only Docker to
be installed.

The environment includes:

- PHP 8.2 with Apache
- MySQL 8.0
- PostgreSQL
- Xdebug 3.4.5
- Symfony CLI

## Getting Started

### Quick Start

The fastest way to start the environment:

1. Clone this repository
2. Run `make start` from the project root directory

This will set up and start all required containers automatically.

### Prerequisites

- Docker Engine 20.10 or later
- Docker Compose V2
- Make
- Git (optional, for version control)

### Installation

1. Clone this repository to your local machine
2. Navigate to the `.docker/docker-compose` directory
3. Create a `.env` file from `.env.example` (if needed) and adjust UID/GID values
   to match your host machine's values
   (run `id -u` for UID and `id -g` for GID)
4. Run `make start` to start the environment

## Usage

The environment will be available at http://localhost:8080

Common commands:

- Start environment: `make start`
- Stop environment: `make down`
- Access PHP container: `make bash`
- Check container logs: `make logs`

Database connections:

- MySQL: localhost:3306 (user: app, password: app)
- PostgreSQL: localhost:5432 (user: app, password: app)


## License

This project is licensed under the [MIT License].
