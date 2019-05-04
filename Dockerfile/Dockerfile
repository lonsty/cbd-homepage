FROM python:3.5.2

WORKDIR /flasky

ADD ./flasky /flasky

ENV FLASK_APP "flasky"
ENV FLASK_CONFIG "production"

RUN pip install -r requirements.txt && cp /usr/share/zoneinfo/Hongkong /etc/localtime

EXPOSE 80

CMD ["python", "manage.py", "runserver", "-h", "0.0.0.0", "-p", "80"]