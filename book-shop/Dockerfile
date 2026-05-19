FROM python:3.11-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /app

RUN apt-get update && apt-get install -y libpq-dev gcc && rm -rf /var/lib/apt/lists/*

COPY app-artifact.tar.gz /tmp/
RUN tar -xzf /tmp/app-artifact.tar.gz -C /app/ && rm /tmp/app-artifact.tar.gz

RUN pip install psycopg2-binary

EXPOSE 8000