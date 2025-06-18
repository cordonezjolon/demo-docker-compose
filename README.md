# Demo Docker Compose Express API

This project provides a simple Express API with two endpoints:

- `GET /health` — Health check endpoint.
- `GET /hello?name=YourName` — Greets the provided name.

## Running Locally

1. Install dependencies:
   ```sh
   npm install
   ```
2. Start the server:
   ```sh
   npm start
   ```

## Docker & Docker Compose

To build and run with Docker Compose (5 replicas, load balanced):

```sh
docker compose up --build --scale api=5
```

The API will be available at [http://localhost:8080](http://localhost:8080)

## Endpoints

- `/health` — Returns `{ status: "ok" }`
- `/hello?name=YourName` — Returns `{ message: "Hello, YourName!" }`
