# Use the latest Ubuntu image as the base image
FROM ubuntu:latest

# Update and upgrade the package lists
RUN apt-get update && \
    apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix the EXTERNALLY-MANAGED error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask
RUN pip3 install flask

# Set the working directory
WORKDIR /app

# Copy the Python file into the Docker image
COPY api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]
FROM nginx:latest

COPY softy-pinko-front-end /var/www/html/softy-pinko-front-end
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

EXPOSE 9000
