# Use Python base image
FROM python:3.10

# Set the working directory inside the container
WORKDIR /app

# Copy all files from your local project to the container
COPY . .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose port (if the app runs on a port, e.g., Flask/Django)
EXPOSE 5000

# Define the command to run the application
CMD ["python", "app.py"]
