FROM jupyter/pyspark-notebook
ENV PYTHONBUFFERED 1
EXPOSE 8888

USER root

COPY ./requirements.txt requirements.txt

RUN sudo apt update && \
    python -m venv /py && \
    /py/bin/pip install --upgrade pip && \
    pip install -r requirements.txt
