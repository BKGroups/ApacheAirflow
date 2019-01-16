Airflow tutorial
This is the code for Airflow-tutorial playlist by Tuan Vu on Youtube

Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Clone this repo
Install the prerequisites
Run the service
Check http://localhost:8080
Done! tada
Prerequisites
Install Docker
Install Docker Compose
Following the Airflow release from Python Package Index
Usage
Run the web service with docker

docker-compose up -d

# Build the image
# docker-compose up -d --build
Check http://localhost:8080/

docker-compose logs - Displays log output
docker-compose ps - List containers
docker-compose down - Stop containers
Other commands
If you want to run other airflow sub-commands, you can do so like this:

docker-compose run --rm webserver airflow list_dags - List dags
docker-compose run --rm webserver airflow test [DAG_ID] [TASK_ID] [EXECUTION_DATE] - Test specific task
Connect to database
If you want to use Ad hoc query, make sure you've configured connections: Go to Admin -> Connections and Edit "postgres_default" set this values:

Host : postgres
Schema : airflow
Login : airflow
Password : airflow
Credits
Apache Airflow
docker-airflow
