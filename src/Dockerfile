# Dockerfile

# FROM directive instructing base image to build upon
FROM python:2

RUN mkdir /code
WORKDIR /code
ADD requirements.txt /code/
RUN pip install -r requirements.txt
ADD . /code/


# EXPOSE port 8000 to allow communication to/from server
EXPOSE 8000

WORKDIR /code/helloworld

# CMD specifcies the command to execute to start the server running.
CMD ["../start.sh"]
# done!
