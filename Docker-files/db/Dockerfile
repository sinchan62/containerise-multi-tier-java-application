FROM mysql:8.0.33
LABEL "project"="vprofile"
LABEL "author"="rrohit62"

ENV MYSQL_ROOT_PASSWORD="vprodbpass"
ENV MYSQL_DATABASE="accounts"

# Add the SQL backup file to the container's initialization directory
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql