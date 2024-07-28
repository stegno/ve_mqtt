# Use an official Python runtime as a parent image
#FROM python:3.9.6
FROM python:3.11.8
# Set the working directory in the container
WORKDIR /app

# Copy the .whl file into the container at /app
COPY asyncio_vedirect_mqtt-1.2.0-py3-none-any.whl /app/

# Install the Python package from the .whl file
RUN apt-get update && \
    apt-get install -y python3-pip
RUN pip3 install asyncio_vedirect_mqtt-1.2.0-py3-none-any.whl

# Run the command to start your application
CMD ve-mqtt -v --tty /dev/ttyVICTRON --broker 127.0.0.1 --port 1883 --username ve-mqtt --password mqtt --device victron
