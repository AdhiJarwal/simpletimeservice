FROM python:3.11-slim

RUN addgroup --system appgroup && \
    adduser --system --group appuser

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY app.py .

USER appuser

EXPOSE 8080

CMD ["python", "app.py"]
