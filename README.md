# Garage Rent

This is a garage rent management project, developed with TypeScript, Express, PostgreSQL running on a Docker container, and Prisma.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Configuration](#configuration)
- [Scripts](#scripts)
- [Project Structure](#project-structure)
- [API Routes](#api-routes)
- [Data Model](#data-model)
- [License](#license)

## Introduction

This project aims to provide an API to manage garage rents, allowing the creation, reading, updating, and deletion of garage information.

## Installation

To start using this project, follow the steps below:

1. Clone the repository:

    ```sh
    git clone https://github.com/https://github.com/vinimostaco/garage-rent.git/garage-rent.git
    cd garage-rent
    ```

2. Install dependencies:

    ```sh
    npm install
    ```

3. Set up the PostgreSQL database and add the connection URL to the `.env` file.

## Configuration

1. Create a `.env` file in the project root and add the following environment variables:

    ```env
    DATABASE_URL="postgresql://admin:admin123@localhost:6000/prisma-teste?schema=public"
    PORT=3000
    ```

2. Set up Prisma:

    ```sh
    npx prisma migrate dev --name init
    npx prisma generate
    ```

## Scripts

In the `package.json` file, you will find the following scripts:

- `start:dev`: Starts the server in development mode using `ts-node`.
- `db`: Starts the db in development mode using `docker compose`.
- `build`: Compiles the TypeScript code to JavaScript.
- `start`: Starts the server from the compiled files.

To run the server in development mode, use:

```sh
npm run dev
```

## Project Structure
```
garage-rent/
├── prisma/
│   ├── migrations/
│   ├── schema.prisma
│   └── seed.ts
├── src/
│   ├── config/
│   │   └── db.ts
│   ├── controller/
│   │   └── garage-controller.ts
│   ├── routes/
│   │   └── garage-routes.ts
│   ├── services/
│   │   └── garage-service.ts
│   ├── utils/
│   ├── app.ts
│   └── server.ts
├── .env
├── .gitignore
├── package.json
├── README.md
└── tsconfig.json
```

## Directory and File Descriptions

- `prisma/`: Contains Prisma configuration, including the database schema.
- `src/config/`: Configuration and initialization of the Prisma client.
- `src/controller/`: Contains controllers that handle HTTP requests.
- `src/routes/`: Defines application routes.
- `src/models/`: Defines TypeScript types for data models.
- `src/services/`: Contains business logic and complex operations.
- `src/app.ts`: Sets up and exports the Express application.
- `src/server.ts`: Starts the Express server.

