Real-Time Weather Data ETL System
This project is an end-to-end automated pipeline for extracting, transforming, and loading real-time weather data using modern data engineering tools. It demonstrates ETL orchestration with Apache Airflow, data integration and storage with PostgreSQL, and validation with DBeaver—all containerized for reproducibility and ease of deployment.

Project Overview
Extraction: Fetches real-time weather data from public APIs for specific locations using Python.

Transformation: Cleans and processes the raw weather data to ensure consistency and usability.

Loading: Inserts the processed data into a PostgreSQL database for storage and analysis.

Orchestration: Utilizes Apache Airflow to schedule, manage, and automate daily ETL workflows.

Containerization: All components, including Airflow and PostgreSQL, are containerized using Docker for easy setup, scalability, and reproducibility across environments.

Verification: Uses DBeaver as a visual client to connect to PostgreSQL, query tables, and verify loaded data.

Project Structure
dags/
Contains your custom Python Airflow DAG(s) for the weather data ETL pipeline.

Dockerfile
Specifies the environment for running Airflow and ETL dependencies (Python, Airflow, etc.).

requirements.txt
Lists required Python libraries for the project (e.g., requests, psycopg2, etc.).

airflow_settings.yaml
Manages Airflow connections, variables, and configuration for local development.

Running Locally
Prerequisites:

Install Docker and Docker Compose.

Install the Astronomer CLI (astro).

Steps:

Clone this repository.

From the project root directory, run:

text
astro dev start
Airflow will be available at http://localhost:8080 (default credentials: admin/admin).

PostgreSQL database is accessible at localhost:5432/postgres (user: postgres, password: postgres).

Use DBeaver (or another client) to connect to the database, verify and explore the weather data tables.

Customizing the Pipeline
To modify locations or APIs, update the Python scripts in the dags/ directory.

Adjust scheduling or workflow logic using Airflow’s UI or by editing DAG file parameters.

Credits
Developed as an independent data engineering project using open-source tools to demonstrate practical ETL and orchestration workflows.

Contact
For questions or suggestions about this project, please open an issue in the repository or reach out directly.
