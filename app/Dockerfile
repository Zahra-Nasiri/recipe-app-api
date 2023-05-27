FROM python:3.9-alpine3.13
LABEL maintainer = "Zahra Nasirmohammadi"

ENV PYTHONUNBUFFERED 1
EXPOSE 8000
ARG DEV=false

WORKDIR /app
COPY . .

RUN <<EOF 
    apk add --update --no-cache postgresql-client jpeg-dev  
    apk add --update --no-cache --virtual .temp-build-deps build-base postgresql-dev musl-dev zlib zlib-dev 
    pip3 install -r requirements.txt
    if [ $DEV = "true" ]; 
      then pip3 install -r requirements.dev.txt ; 
    fi  
    apk del .temp-build-deps build-base postgresql-dev musl-dev zlib zlib-dev 
    adduser --disabled-password  --no-create-home  django-user 
    mkdir -p /vol/web/media 
    mkdir -p /vol/web/static 
    chown -R django-user:django-user /vol
    chmod -R 755 /vol
EOF



USER django-user
