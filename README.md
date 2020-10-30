Laravel on FHIR
================

## Configure Database

These are the steps to connect to the CockroachDB insecure cluster running locally

1. Install postgresql driver `sudo apt-get install php7.3-pgsql`
2. Run database cluster with docker-compose `docker-compose up`
3. STart a new terminal session in one node of the cluser `docker exec -it <COCKROACH_DB_NODE_CONTAINER_ID> bash`
4. Start a new SQL session `cockroach sql --insecure`
5. Create the database `CREATE DATABASE laravel_on_fhir;`
6. Exit from sql and container and then run the migrations `php artisan migrate`