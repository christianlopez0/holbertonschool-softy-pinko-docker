# Use the official Nginx image from the Docker Hub
FROM nginx:latest

# Copy the Nginx configuration file
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

# Copy the front-end code to the Nginx web directory
COPY softy-pinko-front-end /usr/share/nginx/html

# Expose the port Nginx runs on
EXPOSE 80
