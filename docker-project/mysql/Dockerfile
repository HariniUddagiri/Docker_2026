FROM mysql:8.0
#when we are using docker official imgae, that documentation has to be referred for the environment variables that can be set.
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
#As per docker official documentation of a sepecific image, if we want to run any sql scripts during the container startup, we need to copy those scripts to /docker-entrypoint-initdb.d location. The scripts will be executed in alphabetical order.
COPY scripts/*.sql /docker-entrypoint-initdb.d 

