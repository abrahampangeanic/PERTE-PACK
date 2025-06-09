# PERTE PACK

This repository provides a complete setup of an application composed of two services:

- **App Front** as a frontend application.
- **App API** as a backend application.

## Prerequisites

Before running the application, ensure that you have the following installed:

- Docker
- Docker Compose

## Project Structure

The project structure is organized with two main directories for the applications and a `docker-compose.yml` file for service configuration.

```plaintext
.
├── front/                   # App Front application source code
│   ├── .env
│   └── Dockerfile
├── strapi/                  # App API application source code
│   ├── .env 
│   └── Dockerfile
├── docker-compose.yml          # Docker Compose service configuration
└── README.md                   # This file
```

## Environment Configuration

To customize the configuration, create an `.env` file in the project root directory with the following variables (if they don’t already exist in your project):


## Building and Running the Project

### Step 1: Build the Containers

From the project root directory, run the following command to build all services:

```bash
docker-compose up --build
```

