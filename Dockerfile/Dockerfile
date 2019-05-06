FROM python:3.7.1

WORKDIR /CBDHomepage

ADD ./CBDHomepage /CBDHomepage

ENV FLASK_APP "CBDHomepage"
ENV FLASK_CONFIG "production"

RUN pip install -r requirements.txt && cp /usr/share/zoneinfo/Hongkong /etc/localtime

EXPOSE 80

CMD ["python", "manage.py", "runserver", "-h", "0.0.0.0", "-p", "80"]
