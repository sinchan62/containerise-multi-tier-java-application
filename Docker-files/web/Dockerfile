FROM nginx
LABEL "project"="vprofile"
LABEL "author"="rrohit62"

# Remove the default Nginx configuration file
RUN rm -rf /etc/nginx/conf.d/default.conf

# Copy the custom Nginx configuration file into the container
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf