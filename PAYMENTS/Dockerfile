# Use an official Pyhton image as the base image
FROM python:3.9-alpine

#Use an workdi as /app
WORKDIR /app

#Copy the shipping project and source code
COPY requirements.txt . \
     *.py . \
    payment.ini .

# INSTALL THE REQUIREMENTS
RUN apk --no-cache add build-base linux-headers
RUN pip install --upgrade setuptools
RUN pip install -r requirements.txt

# Setting up environment variables
ENV AMQP_USER=roboshop \
    AMQP_PASS=roboshop123

# Specify the command to run the application
CMD ["uwsgi", "--ini", "payment.ini"]
