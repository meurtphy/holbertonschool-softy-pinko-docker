FROM ubuntu:latest

RUN apt-get update && apt-get install -y python3 python3-pip
RUN pip3 install --break-system-packages flask flask-cors

WORKDIR /app

COPY ./api.py /app/api.py

CMD ["python3", "/app/api.py"]
