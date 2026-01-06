FROM python:3.14-slim

RUN pip install --no-cache-dir flask paho-mqtt confluent_kafka
WORKDIR /app

COPY accumulator-server.py /app/accumulator-server.py
EXPOSE 1028

CMD ["python", "accumulator-server.py", "--port", "1028", "--url", "/accumulate", "--host", "0.0.0.0", "--pretty-print", "-v"]
