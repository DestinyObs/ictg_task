# Use an official Python runtime as a parent image
FROM python:3.12-slim

#install poetry
RUN pip install poetry

# Set the working directory
WORKDIR /app

#copy the rest of the application code
COPY pyproject.toml poetry.lock ./

# Install dependencies using Poetry
RUN poetry install --no-root

#copy the rest of the application code
COPY . .

ENV PYTHONPATH=/app

CMD poetry run bash ./prestart.sh; poetry run uvicorn app.main:app --host 0.0.0.0 --port 8000