FROM python:3.12.2-slim

WORKDIR /weather_app
COPY . /weather_app

RUN pip install -r requirements.txt && \
pip install gunicorn && mkdir history

EXPOSE 8080

CMD gunicorn --bind=0.0.0.0:8080 weather_server:app
