FROM python:3.7.4

RUN mkdir /src

COPY ./requirements.txt /src/requirements.txt
RUN pip install -r /src/requirements.txt

COPY . /src/
WORKDIR /src

CMD gunicorn --bind :$PORT --workers=2 index:app
