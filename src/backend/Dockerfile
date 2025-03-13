FROM ubuntu:22.04

# Install Python 3.9 and pip
RUN apt-get update && \
    apt-get install -y python3.9 python3-pip

# Set the working directory
WORKDIR /app

# Copy the requirements file
COPY requirements.txt .

# Install the dependencies
RUN pip install -r requirements.txt

# Copy the contents of the current directory
COPY . .

# Expose the port
EXPOSE 8000

# Set the command to run the FastAPI app
CMD ["python3", "./main.py"]
