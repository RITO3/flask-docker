FROM python:3.8-buster

WORKDIR /opt/app

ENV PYTHONPATH /opt/app

COPY . .

RUN pip install -r requirements.lock

RUN useradd -r -s /bin/false uwsgiusr

USER uwsgiusr

EXPOSE 8000

CMD ["uwsgi", "--ini", "/opt/app/uwsgi.ini"]