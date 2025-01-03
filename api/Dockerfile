FROM python:3.9

WORKDIR /app

COPY Pipfile Pipfile.lock ./

EXPOSE 5050

RUN pip install pipenv

RUN pipenv requirements


RUN pipenv lock > requirements.txt

RUN pip install requests

RUN pip install flask

RUN pip install jinja2

RUN pip install python-dotenv

RUN pip install flask-cors

COPY . ./

CMD [ "python" , "main.py"]

