FROM python:3.7.6

WORKDIR /src

COPY requirements.txt /src/requirements.txt
RUN pip install -r requirements.txt

COPY lib/requirements.txt /src/lib/requirements.txt
RUN pip install -r lib/requirements.txt

COPY server.py /src/
COPY lib /src/lib/

RUN useradd docker
USER docker

EXPOSE 6324

CMD ["python", "server.py"]
