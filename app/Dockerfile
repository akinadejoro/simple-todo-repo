FROM python:3.8-buster

WORKDIR /app

# RUN apt-get update && apt-get install -y tzdata && apt install -y python3.8 python3-pip

COPY requirements.txt requirements.txt

RUN pip3 install --upgrade pip

RUN pip3 install -r requirements.txt

COPY . .

EXPOSE 8000

# CMD  ["python3", "manage.py", "runserver", "0.0.0.0:8000"]

ENTRYPOINT ["python3", "manage.py"]
CMD ["runserver", \
        "0.0.0.0:8000"]