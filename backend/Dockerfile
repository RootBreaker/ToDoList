FROM python:3.10-alpine

ENV PYTHONUNBUFFERED 1

RUN apk update \
   && apk add postgresql-dev gcc python3-dev musl-dev
RUN pip install --upgrade pip pipenv
RUN pip3 install pipenv==v2022.4.20

WORKDIR /backend
COPY requirements.txt ./
RUN pip install -r requirements.txt
RUN pip3 install --upgrade pip
RUN pip3 install pipenv
COPY Pipfile* .
# Install dependencies
RUN pipenv lock && pipenv --clear && pipenv --rm
RUN pipenv install --system --deploy

COPY . .

COPY ./entrypoint.sh /entrypoint.sh
RUN chmod o+x /entrypoint.sh

ENTRYPOINT ["sh", "-c", "/entrypoint.sh"]