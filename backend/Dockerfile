# Use Python image
FROM python:3.10

# Environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Working directory
WORKDIR /app

# Copy requirements
COPY requirements.txt .

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy project files
COPY . .

# Create folders
RUN mkdir -p instance uploads

# Expose Flask port
EXPOSE 5000

# Start Flask
CMD ["python", "app.py"]