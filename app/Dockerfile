# Use the appropriate Python base image
FROM python:3.11-slim

# Set the working directory
WORKDIR /app

# Copy requirements file
COPY requirements.txt /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . /app/

# Command to run the application
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "your_app_module:app"]
