This repository contains a [Camouflage](https://testinggospels.github.io/camouflage)-based mock server used for training purposes.

## Setup

Install the dependencies:

```shell
yarn
```

## Usage

To start the mock server, use

```shel
yarn start
```

It will come up on http://localhost:8080.

## Predefined routes

Some predefined routes are in place to support training:

- `POST /login`: Mocks a login and returns an access token:

  ```sh
  $ curl -X POST \
    --data '{"username": "user", "password": "pw"}' \
    http://localhost:8080/login

  { "accessToken": "abc" }
  ```

- `GET /profile`: Returns a mock user profile:

  ```sh
  $ curl http://localhost:8080/profile

  { "profile": { "firstName": "John", "lastName": "Doe", "jobTitle": "COBOL Architect" }}
  ```

## Adding new routes

To add new routes, use the `mock` folder.
