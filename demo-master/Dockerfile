# Use Python base image
FROM python:3.10

# Set the working directory inside the container
WORKDIR /app

# Copy only Pipfile and Pipfile.lock first
COPY Pipfile Pipfile.lock .  

# Install Pipenv and dependencies
RUN pip install --no-cache-dir pipenv && pipenv install --deploy --ignore-pipfile

docker build -t my-app .
COPY . .

# Expose port (modify based on your app)
EXPOSE 5000

# Define the command to run the application
CMD ["python", "app.py"]
