FROM ubuntu:20.04

RUN apt-get update -y
RUN apt-get install python3.8 -y
RUN apt-get install python3-pip -y
RUN ln -s /usr/bin/python3 /usr/bin/python

WORKDIR /sandbox

RUN pip3 install requests python-magic numpy

CMD pip3 install -r requirements.txt \
    & echo 127.0.0.1 example1.ge example2.ge example3.ge example4.ge example5.ge >> /etc/hosts \
    & /bin/bash