# Spark Cluster on Docker Environment

## Overview

Apache Spark is a powerful open-source processing engine built around speed, ease of use, and sophisticated analytics.
This project provides a Dockerized environment for running a Spark cluster, allowing for easy setup and management.

## Features

- **Spark Master and Worker Nodes:**
  - A master node for managing the cluster.
  - Worker nodes for processing tasks.

## Prerequisites

Before running the project, ensure you have:

- [Docker Desktop](https://www.docker.com/products/docker-desktop) (includes Docker Compose)
- At least 4GB of RAM recommended for optimal performance

## Setup Instructions

1. **Clone the Repository:**
   Clone the repository to your local machine:

   ```bash
   git clone https://github.com/hiltonmbr/spark-docker.git
   ```

2. **Review Configurations:**
   Check and update configuration files and environment variables as needed for your specific setup.

3. **Start the Cluster:**
   Launch your cluster using Docker Compose:

   ```bash
   docker compose up -d
   ```

4. **Verify Services:**
   Once started, check the status of all containers:

   ```bash
   docker compose ps
   ```

## Stopping the Cluster

To stop the cluster, run:

```bash
docker compose down
```

## Accessing the Services

- **Spark Web UI:** Open [http://localhost:8081](http://localhost:8081).
- **Code-Server (Python Notebooks):** Open [http://localhost:8443](http://localhost:8443) to access the code-server interface.

## Troubleshooting

- **Cluster Not Starting:**

  - Ensure Docker Desktop is running.
  - Inspect container logs for errors:

    ```bash
    docker compose logs
    ```

- **Service Access Issues:**

  - Verify that no firewall or network settings are blocking the required ports.
  - Confirm that all containers are running:

    ```bash
    docker compose ps
    ```

## Usage Notebooks with Code-Server

After setting up the environment:

1. Open the Notebook `handle-rdds.ipynb` in the code-server.

2. Select Kernel and install suggested extensions `Python` and `Jupyter`.

3. Select Python Environments and choose Create a Python Virtual Environment (`.venv`).

- Select the option "Python 3.12" and press Enter.
- Wait for the virtual environment to be created.

4. Make sure you have as selected kernel a Python Virtual Environment (`.venv`).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request with any improvements, bug fixes, or suggestions.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
