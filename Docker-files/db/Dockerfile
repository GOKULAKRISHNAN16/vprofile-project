FROM mysql:8.033
LABEL "project"="vprofile"
LABEL "author"="Gokul"

ENV MYSQL_ROOT_PASSWORD="password"
ENV MQSQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb.d/db_backup.sql