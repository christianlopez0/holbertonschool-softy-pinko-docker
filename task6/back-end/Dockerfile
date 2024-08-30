# Use the official Python image from the Docker Hub
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt /app/requirements.txt

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY api.py /app/api.py

# Expose the port the app runs on
EXPOSE 5252

# Command to run the application
CMD ["python", "api.py"]
