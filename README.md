# Playwright Test Automation Project

## Introduction

This project is designed for automated testing using Playwright, a powerful tool for browser automation. It includes a Docker configuration to facilitate seamless setup and execution of tests exporting it to a local volume.

## Prerequisites

Before running the tests, ensure you have Docker installed on your system.

## Setup Instructions

1. Clone this repository to your local machine:

    ```bash
    git clone https://github.com/AlvaroRaul7/playwright-docker.git
    ```

2. Navigate to the project directory:

    ```bash
    cd playwright-docker
    ```

3. Build the Docker image using the provided Dockerfile:

    ```bash
    docker build -t playwright-docker .
    ```

## Running Tests

Once the Docker image is built, you can execute the tests by running the following command:

```bash
docker run -it -v "$(pwd)/playwright-local-report:/app/playwright-report" playwright-docker
```

This command runs the tests inside the Docker container and mounts the `playwright-local-report` directory to `/app/playwright-report` inside the container to save test reports locally.

## Viewing Test Reports

After running the tests, you can find the test reports inside the `playwright-local-report` directory in your project's root folder.

## Notes

- You can customize the test configurations by modifying the relevant files in the project.
- Ensure that your Docker daemon is running while executing the tests.

## Contributors

- [Alvaro Valarezo](https://github.com/AlvaroRaul7)

## License

This project is licensed under the [MIT License](LICENSE).