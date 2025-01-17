# express-wrapper

A wrapper repository that includes ready-to-use Docker and testing frameworks for building production-grade software.

## Components Included

1. **Express** - Web framework for Node.js
2. **Testing Framework**
    1. **Mocha** - Testing framework
    2. **Chai** - Assertion library
    3. **Supertest** - HTTP assertions for testing API endpoints
3. **ESLint** - Linting utility for JavaScript
4. **Prettier** - Code formatter
5. **Winston** - For logging
6. **dotenv** - Environment variable management
7. **Docker** - For containerization

## Steps to Setup Locally

1. **Clone the Repository and Install Packages:**

    ```sh
    git clone <repository-url>
    cd express-wrapper
    npm install
    ```

2. **Setup Environment Variables:**

    Create a [.env](http://_vscodecontentref_/2) file in the root directory and add your environment variables. Example:

    ```env
    PORT=3000
    NODE_ENV=development
    ```

3. **Run the Docker Container:**

    ```sh
    docker-compose up --build
    ```

## Steps to Test

- All tests should be stored under the `tests` folder and should be suffixed with `*.test.js`.
- A `setup.js` file is included in the `tests` folder for setup and teardown.
- Mocha configurations are under [.mocharc.json](http://_vscodecontentref_/1).

### Run Tests

```sh
npm test
```

### Run lint checks

```
npm run lint
```

If you get prettier errors, you can fix them manually or by running this:

```
npx prettier --write .
```

## Run with docker

### 1. Build the Docker Image:

```sh
docker compose build
```

### 2. Run the docker container:

```sh
docker compose up
```

### 3. Stop the docker container

```sh
docker compose down
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License.
