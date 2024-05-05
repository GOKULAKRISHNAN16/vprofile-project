FROM nginx
LABEL "project"="vprofile"
LABEL "author"="Gokul"

RUN rm -f /etc/nginx/conf.d/default.conf
COPY nginxvproapp.conf  /etc/nginx/conf.d/project.conf