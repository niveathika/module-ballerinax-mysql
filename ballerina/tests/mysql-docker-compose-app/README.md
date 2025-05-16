# MySQL Docker Compose Application

This project sets up a MySQL service using Docker and Docker Compose. It includes various SQL scripts for testing different functionalities of the MySQL server and supports SSL connections.

## Project Structure

- **Dockerfile**: Defines the MySQL service configuration, using the MySQL 8.0.40 image. It copies SQL scripts for initialization and sets up SSL certificates and a custom MySQL configuration file.
  
- **docker-compose.yml**: Configures the services, networks, and volumes for the Docker Compose application. It specifies the MySQL service and sets environment variables such as the root password.

- **my.cnf**: Contains custom MySQL configuration settings that will be applied when the MySQL server starts.

- **sql-scripts/**: A directory containing various SQL scripts organized into subdirectories for different test cases:
  - **connection/**: Scripts for connection tests.
  - **pool/**: Scripts for connection pool tests.
  - **execute/**: Scripts for execution tests.
  - **batchexecute/**: Scripts for batch execution tests.
  - **error/**: Scripts for error tests.
  - **query/**: Scripts for query tests.
  - **procedures/**: Scripts for stored procedure tests.
  - **transaction/**: Scripts for transaction tests.

- **keystore/server/**: A directory intended to hold SSL certificate files for secure connections to the MySQL server.

## Setup Instructions

1. Ensure you have Docker and Docker Compose installed on your machine.

2. Clone this repository or download the project files.

3. Navigate to the project directory:
   ```
   cd mysql-docker-compose-app
   ```

4. Build and start the MySQL service using Docker Compose:
   ```
   docker-compose up --build
   ```

5. The MySQL server will be initialized with the provided SQL scripts. You can connect to the MySQL server using the root password specified in the `docker-compose.yml` file.

## Usage Guidelines

- Modify the SQL scripts in the `sql-scripts/` directory as needed for your testing purposes.
- Update the `my.cnf` file for any custom MySQL configuration settings.
- Place your SSL certificate files in the `keystore/server/` directory to enable secure connections.

## License

This project is licensed under the Apache License, Version 2.0. See the LICENSE file for more details.