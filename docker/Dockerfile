FROM ubuntu:20.04
#OS 업데이트
RUN apt-get update -y
RUN apt-get upgrade -y
# RUN apt-get install python3.8 -y
RUN apt-get install iputils-ping -y
# RUN apt-get install python3-pip -y


ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y --no-install-recommends apt-utils

RUN apt-get install -y python3-pip python3-dev build-essential
RUN apt-get install -y libtiff5-dev libjpeg8-dev libopenjp2-7-dev zlib1g-dev \
libfreetype6-dev liblcms2-dev libwebp-dev tcl8.6-dev tk8.6-dev python3-tk \
libharfbuzz-dev libfribidi-dev libxcb1-dev
RUN apt-get install -y libpq-dev python3-dev
RUN apt-get install -y libgl1-mesa-glx


#pip install
# RUN apt-get install -y python-pip python-dev build-essential
# RUN apt-get install -y python3-pip python3-dev build-essential
# RUN apt-get install -y libtiff5-dev libjpeg8-dev libopenjp2-7-dev zlib1g-dev \
# libfreetype6-dev liblcms2-dev libwebp-dev tcl8.6-dev tk8.6-dev python3-tk \
# libharfbuzz-dev libfribidi-dev libxcb1-dev
# RUN apt-get install -y libpq-dev python3-dev
# RUN apt-get install -y libgl1-mesa-glx
RUN apt-get install -y curl
RUN apt-get install -y wget
RUN apt-get install -y openssh-server
RUN apt-get install -y net-tools
RUN apt-get install -y vim
RUN apt-get install -y cron

# RUN apt-get install build-dep python-psycopg2

# RUN pip install --upgrade pip
COPY requirements.txt /txt/
RUN pip3 install -r /txt/requirements.txt 


#지역 설정/ 시간

ENV TZ=Asia/Seoul
RUN apt-get install -y tzdata
#locale 설정
ENV LC_ALL=C.UTF-8
ENV LANGUAGE=ko