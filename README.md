# Weather sensor data package

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the web application](#running-the-web-application)
  - [Running tests](#running-test)
  - [Running Docker](#run-docker)
- [Rest API Documentation](#api-documentation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Weather sensor data storage

A node application that stores data generated by a collection of sensors set up world wide. The sensors send a CSV payload of data which they collect over a period of time.

Technologies used

- Backend: NodeJS & RestAPI & Expressjs using Javascript
- Database: Postgres
- REST API documentation: Swagger UI
- Testing: Jest, Supertest
- CI - Github Actions
- Containerization - Docker

## Features

The service has four major endpoints implemented

- POST "/api/login": This endpoint handles user authentication by validating the provided email and password. Upon successful authentication, a cookie is returned that can be used to authorize subsequent requests.

- POST "/api/sensors/upload": Sensor data is sent to this endpoint for storage. The data is authenticated using the cookie obtained from the login request. CSV data provided in the POST body is stored for later queries.

- POST "/api/sensors/search": This endpoint allows users to retrieve sensor data. Authentication is performed using the previously obtained cookie from the login request.

- POST "/api/register": New users can register using this endpoint. User data, including email and password, can be submitted to create a new account.

The authentication and authorization mechanisms in use (bcrypt, JWT tokens and Cors)

## Getting Started

To run this web application on your local machine, follow the steps below:

### Prerequisites

Before getting started, ensure that you have the following software installed on your machine:

- Node.js: Download and install Node.js from the official website: https://nodejs.org

Before you start the application, you need to set up an environment variable to store your API key. Here's how you can do it:

```bash
PORT=3001
JWT_SECRET="YOUR KEY"
NODE_ENV=development
DEV_USERNAME="DATABASE USERNAME"
DEV_PASSWORD="DATABASE PASSWORD"
DEV_DATABASE="NAME OF DB"
DEV_PORT=5432
DEV_HOST="HOST"
```

Create a file called `.env` in express-backend folder of the project with the environmental variables above. Replace "YOUR KEY","DATABASE USERNAME","DATABASE PASSWORD","NAME OF DB","HOST"with the appropriate values.

### Installation

Step-by-step guide on how to install the project and its dependencies.

1. Clone the repository to your local machine using Git:

```bash
git clone https://github.com/ayofalo/weather-data.git
```

2. Navigate to the project directory

```bash
cd weatherdata
cd express-backend
```

3. Install the project dependencies using NPM(Node Package Manager):

```bash
npm install
```

### Running the web application

Once you have installed the dependencies, you can start the web application using

```bash
npm run start
```

### Running Tests

Once you have installed the dependencies, you can run test within the express-backend directory

- run test express-backend

```bash
cd express-backend
npm run test
```

### Run docker

navigate to the root directory

```bash
cd weatherdata
docker-compose up

```

To stop the containers

```bash
docker-compose stop
```

### API documentation

Access API documentation via Swagger UI using the link below after starting up the application

```bash
http://localhost:3001/api-docs/
```

### Usage

- Using the API: Refer to the Swagger API documentation at http://localhost:3001/api-docs for a detailed list of available endpoints and how to interact with them.

- Troubleshooting
  If you encounter any issues or have questions, please feel free to reach out to us by creating an issue on our GitHub repository: https://github.com/ayofalo/my-news-app/issues.

### License

This project is licensed under the MIT License.

### Authors

Contributors names and contact info

Ayo Folami
