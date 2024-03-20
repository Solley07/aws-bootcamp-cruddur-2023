FROM python:3.10-slim-buster
# Inside Container
# Make a new folder inside the container
WORKDIR /backend-flask

# Outside COntainer -> Inside the container
# This containe the library used for the app
COPY requirements.txt requirements.txt
# inside container 
# Install python
RUN pip3 install -r requirements.txt

COPY . .
# SET Environment Variables (Env Vars)
ENV FLASK_ENV=development

EXPOSE ${PORT}
# python -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]