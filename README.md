# Waterfall_Drupal

## Aquia Drupal 10 Site Builder Course - Waterfall Handbook Project

Welcome to the repository for the Waterfall Handbook project, created as part of the Aquia Drupal 10 Site Builder Course.

## Prerequisites

Before you can run this project, please ensure that you have the following prerequisites installed on your system:

- **Docker**: Docker is a containerization platform used to run applications in isolated environments. You can download and install Docker from [here](https://www.docker.com/get-started).

- **Docker Compose**: Docker Compose is a tool for defining and running multi-container Docker applications. It is typically included with Docker on most platforms. However, you can verify its installation by running `docker-compose --version` in your terminal.

## Getting Started

To explore our Waterfall Handbook website, follow these steps:

1. **Clone this repository to your local machine using**:

```
git clone https://github.com/26shyamaladevi/Waterfall_Drupal
cd Waterfall_Drupal
```

2. **Run the Docker Compose stack**:

`docker-compose up -d`

- This command will start the Docker containers needed to run the Drupal website.

3. **Access the website**:

- Once the Docker containers are up and running, you can access the Waterfall Handbook website in your web browser at `http://localhost`.

4. **Database Import**:

- Import a database from an SQL dump file (`database_dump.sql`) to a Drupal database. Follow these steps to perform the import:

- **Drop the Current Database (Optional) & Import DB:**

  - If you want to replace the existing database with the new data from the dump file, you can use the `drush sql-drop` command to drop the current database. Be cautious as this will erase all data in the database.

  ```bash
  drush sql-drop -y
  drush sql-cli < ./src/web/database_dump.sql
  ```

5. **Import Config**:

- Import configuration changes into your Drupal site:

```bash
 drush config:import
```

- Clear the Cache (if needed):

  - After importing configuration changes, it's a good practice to clear the cache to ensure that the changes take effect:

    ```bash
    drush cache:rebuild
    ```

6. **Explore the Handbook**:

- Use the website's navigation to explore the Waterfall Handbook.
