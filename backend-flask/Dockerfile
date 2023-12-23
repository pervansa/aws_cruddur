FROM python:3.10-slim-buster

# Inside container, make a new folder inside the container
WORKDIR /backend-flask

# outside container --> inside container
# int contains library we want to install
COPY requirements.txt requirements.txt

# install python lib
RUN pip install -r requirements.txt

COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=4567

CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]