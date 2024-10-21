# **Realtime-Change-Data-Capture-Streaming-CDC**

## **Overview**

The **Change Data Capture (CDC)** with `Debezium`, `Kafka`,` Postgres`, and `Docke`r project provides a scalable and efficient solution for real-time data streaming and processing. By harnessing the power of Debezium for capturing database changes and Kafka for message brokering, this project ensures seamless data flow between systems. PostgreSQL serves as the reliable data source, while Docker simplifies deployment through containerization. This architecture empowers organizations to respond swiftly to data changes, enhancing operational efficiency and decision-making capabilities. `Designed for flexibility and scalability, it is ideal for modern data-driven applications`.


## System Architecture


## Prerequisites

Before running this project, ensure you have the following installed:

- **Python 3.9+**: The programming language used for the application.
- **`psycopg2` library**: A PostgreSQL adapter for Python to facilitate database interactions.
- **`faker` library**: A Python package for generating fake data for testing and development purposes.
- **PostgreSQL server**: A relational database management system running locally or accessible remotely.
- **Docker and Docker Compose**: Tools for containerization and orchestration of services, allowing for an isolated and reproducible environment.

## Installation

1. **Install Required Python Libraries:**

   You can install the required libraries using pip:

   ```bash
   pip install psycopg2-binary faker
   ```

## **Services in the Compose File :**

This project utilizes the following services defined in the Docker Compose file to facilitate real-time change data capture and streaming:

- **Zookeeper:** A centralized service that manages configuration information, naming, distributed synchronization, and group services essential for maintaining the Kafka ecosystem.

- **Kafka Broker:** A robust distributed streaming platform designed to handle real-time data feeds, enabling the seamless transmission of messages between producers and consumers.

- **Confluent Control Center:** A comprehensive web-based interface for managing and monitoring Apache Kafka, providing insights into data flow, performance metrics, and system health.

- **Debezium:** An open-source distributed platform that captures changes in database records, allowing for efficient tracking of data modifications in real-time.

- **Debezium UI:** A user-friendly interface that facilitates the management and monitoring of Debezium connectors, providing visibility into the status and configuration of change data capture processes.

- **PostgreSQL:** An advanced open-source relational database management system that serves as the primary data source for this project, supporting efficient storage and retrieval of structured data.


## Getting Started

1. **Clone the Repository:**
   Ensure you have this Docker Compose file in your local system. If it's part of a repository, clone the repository to your local machine.


    git clone https://github.com/Atharv-Nanaware/Realtime-Change-Data-Capture-Streaming-CDC
    cd Realtime-Change-Data-Capture-Streaming-CDC

2. **Navigate to the Directory:**
   Open a terminal and navigate to the directory containing the Docker Compose file, ensuring you are in the correct context to execute the subsequent commands.

3. **Run Docker Compose:**
   tart all services defined in the Docker Compose file by executing the command below:

    ```bash
    docker-compose up -d
    ```

   This command will download the required Docker images, create the necessary containers, and start the services in detached mode, allowing them to run in the background.


4. **Verify the Services:**
   Confirm that all services are up and running by checking the status with the following command:

   ```bash
   docker-compose ps
   ```

   You should see a list of services, each marked as 'running', indicating that they have been successfully initialized..

5. **Accessing the Services:**
   - Kafka Control Center is accessible at `http://localhost:9021`.
   - Debezium UI is accessible at `http://localhost:8080`.
   - Postgres is accessible on the default port `5432`.

6. **Shutting Down:**
   To stop and remove the containers, networks, and volumes, run:

   ```bash
   docker-compose down
   ```


