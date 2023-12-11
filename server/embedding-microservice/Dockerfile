FROM python:3.11.3-slim
ENV PYTHONUNBUFFERED 1

WORKDIR /embedding_service/

RUN pip install pip==23.3.1
RUN pip install pip-tools==7.1.0

RUN mkdir model_files/
#RUN git clone https://huggingface.co/intfloat/e5-base-v2 model_files

ADD requirements.txt .
RUN pip-sync requirements.txt  

ADD . .