# syntax=docker/dockerfile:1

# Inherits from base image which contains Python tools and packages
FROM python:3.8-slim-buster

#Sets wording directory app as default location for all commands to follow
WORKDIR /app

# Copies requirements.txt file into image
COPY requirements.txt requirements.txt

# Executes pip install to install requirements.txt into image
RUN pip3 install -r requirements.txt

# Copies source code(directory files) into image
COPY . .

# Gives Docker commands to run
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0"]