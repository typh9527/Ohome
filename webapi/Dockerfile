FROM resin/armv7hf-debian

MAINTAINER joliu<joliu@s-an.org>

COPY requirement.txt requirement.txt

RUN apt-get update && apt-get install -y python python-pip

RUN pip install -r requirement.txt 

RUN pip install flask-cors -i https://pypi.douban.com/simple
RUN mkdir webAPI

ADD webAPI/ webAPI/

CMD python webAPI/app.py
