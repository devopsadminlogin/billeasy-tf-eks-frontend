FROM python:3.9-slim

WORKDIR /app

# Copy the requirements file first
COPY requirements.txt /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . /app

# Command to run the application
CMD ["gunicorn", "--bind", "0.0.0.0:80", "app:app"]


