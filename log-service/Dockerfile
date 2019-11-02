FROM python:3

LABEL "maintainer"="gautur16@ru.is, benediktt16@ru.is"

COPY . /app
WORKDIR /app

ENV PYTHON_ENV production

RUN pip3 install -r requirements.txt

EXPOSE 5002
CMD python ./app.py