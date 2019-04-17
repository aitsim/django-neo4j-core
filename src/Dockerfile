FROM python:alpine3.6
ENV PYTHONUNBUFFERED 1
RUN apk add  --update make automake gcc g++ subversion python3-dev

RUN mkdir /NeoApp;
WORKDIR /NeoApp

ADD requirements.pip /NeoApp
RUN pip install --upgrade pip
RUN pip install -r /NeoApp/requirements.pip
RUN python -m nltk.downloader punkt  && python -m nltk.downloader stopwords



COPY . NeoApp

# Install bash
RUN apk add --no-cache bash gawk sed grep bc coreutils
