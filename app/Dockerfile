FROM python:3.11-slim

WORKDIR /app

COPY main.py .
COPY templates/ ./templates/

RUN pip install fastapi uvicorn jinja2

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
