# Pull the base image
FROM python:3.8

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN mkdir /code
RUN mkdir /code/backend
WORKDIR /code/backend
#Upgrade pip
RUN pip install pip -U
RUN pip install --upgrade setuptools
RUN apt-get update
RUN apt-get install python3 vim gettext -y
RUN pip install uwsgi
ADD . /code/backend


#Install dependencies
RUN pip install -r requirements.txt
EXPOSE 8000
# RUN /usr/sbin/service cron start