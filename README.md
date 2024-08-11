# Japan Visa Analysis

This project is focused on analyzing and visualizing visa issuance data in Japan. The project involves downloading, processing, and visualizing data using various tools and scripts.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Python 3.x**: The project uses Python for data processing and analysis.
- **Docker and Docker Compose**: Required for containerizing and running services.
- **Spark**: Needed for distributed data processing. This is included in the Docker setup, but if not using Docker, ensure Spark is installed.
- **Required Python packages**: Listed in `requirements.txt`.

## Setup Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/japan-visa-analysis.git
   cd japan-visa-analysis
## Install Dependencies

Navigate to the `src` directory and install the required Python packages:

```bash
cd src
pip install -r requirements.txt
```

## Set Up Docker Containers

The project uses Docker for running services. Ensure you have Docker and Docker Compose installed and configured on your local machine or virtual machine.

**Note**: If Docker is running on a virtual machine in Microsoft Azure, ensure you can access the VM and that Docker is properly configured.

Start the Docker containers using Docker Compose:

```bash
docker-compose up -d
```

This will start the required services in detached mode.

## Access the Services

- **Kafka Control Center**: Access at [http://localhost:9021](http://localhost:9021) to monitor Kafka topics and brokers.
- **Debezium UI**: Access at [http://localhost:8070](http://localhost:8070) to manage Debezium connectors.
- **PostgreSQL Database**: Connect to `localhost:5432` using any PostgreSQL client with the credentials provided in the environment configuration.

## Best Practices

- **Data Security**: Ensure that sensitive data is encrypted both in transit and at rest. Use secure methods to manage credentials and access control.
- **Monitoring**: Regularly monitor Kafka and Debezium connectors to ensure that data is being captured and streamed correctly.
- **Resource Management**: Adjust resource allocation (CPU, memory) for Docker containers based on data volume and processing requirements.
