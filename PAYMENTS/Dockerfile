# Use an official Pyhton image as the base image
FROM python:3.9-alpine

#Use an workdi as /app
WORKDIR /app

#Copy the shipping project and source code
COPY requirements.txt . \
    * .py . \
    payment.ini .

# INSTALL THE REQUIREMENTS
RUN pip3.6 install -r requirements.txt

# Specify the command to run the application
CMD ["uwsgi", "--ini", "payment.ini"]
