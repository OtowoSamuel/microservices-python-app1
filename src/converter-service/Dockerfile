FROM python:3.10-alpine

RUN apk add --no-cache \
    build-base \
    postgresql-dev \
    ffmpeg \
    && pip install --no-cache-dir --upgrade pip

WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .

CMD ["python", "consumer.py"]