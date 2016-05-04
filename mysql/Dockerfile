FROM mysql:5.6

ENV MYSQL_ROOT_PASSWORD=root \
    MYSQL_DATABASE=openmrs \
    MYSQL_USER=openmrs \
    MYSQL_PASSWORD=openmrs

RUN apt-get update && apt-get install -y curl unzip; \
    curl -L http://sourceforge.net/projects/openmrs-refapp-docker/files/v2.3.1/openmrs-refapp-database.sql.zip/download \
         -o /tmp/openmrs-refapp-database.sql.zip; \
    unzip /tmp/openmrs-refapp-database.sql.zip -d /docker-entrypoint-initdb.d; \
    rm /tmp/openmrs-refapp-database.sql.zip
