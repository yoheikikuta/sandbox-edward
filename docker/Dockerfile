FROM python:3.6
MAINTAINER Yohei Kikuta <diracdiego@gmail.com>

# Set up envirnment.
RUN apt-get update && apt-get install -y \
    iproute2

# Install python modules.
#COPY ./requirements.txt /requirements.txt
#RUN pip install -r /requirements.txt
COPY ./requirements.in /requirements.in
RUN pip install -r /requirements.in

# Assume ubuntu user id is 1000.
RUN useradd docker -u 1000 -s /bin/bash -m
USER docker

# Set working directory.
WORKDIR /work

CMD ["/bin/bash"]
