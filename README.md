# Liquibase Database Project

This project is designed to demonstrate the use of Liquibase for managing database changes in a CI/CD pipeline using GitHub Actions. 

## Project Structure

- **changelog/**: Contains all changelog files and changesets.
  - **db.changelog-master.yaml**: The main changelog file that defines the sequence of changesets to be applied.
  - **changesets/**: Directory containing individual changeset files.
    - **001-create-tables.sql**: SQL statements to create necessary tables in the database.
    - **002-insert-data.sql**: SQL statements to insert initial data into the created tables.
    - **changelog.yaml**: Additional changesets or references to other changesets for modular organization.

- **.github/workflows/**: Contains the GitHub Actions workflow configuration.
  - **liquibase.yml**: Defines the CI/CD workflow for connecting to the database, testing the connection, and executing Liquibase commands.

- **liquibase.properties**: Configuration properties for Liquibase, including database connection details and changelog file location.

## Getting Started

1. **Database Setup**: Ensure you have a database set up and accessible. Update the `liquibase.properties` file with your database connection details.

2. **Running Liquibase Locally**: You can run Liquibase commands locally to apply changesets. Use the following command:
   ```
   liquibase update
   ```

3. **CI/CD Integration**: The GitHub Actions workflow defined in `.github/workflows/liquibase.yml` will automatically run on specified events (e.g., push, pull request) to apply changes to the database.

## Additional Information

For more detailed information on Liquibase commands and configurations, refer to the [Liquibase documentation](https://www.liquibase.org/documentation/index.html). 

Feel free to contribute to this project by adding new changesets or improving the existing workflow!