# Base Image 
FROM python:2.7-stretch
# Maintainer of image
MAINTAINER morithibaud (morithibaud@gmail.com)
# COPY source code
COPY student_age.py /
COPY student_age.json /data/
# Install packages
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv
# Create Data Volume
VOLUME ["/data"]
# EXPOSE PORT
EXPOSE 5000
# START CODE
CMD [ "python", "./student_age.py" ]