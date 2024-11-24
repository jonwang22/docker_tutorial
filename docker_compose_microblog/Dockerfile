FROM python:3.9

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt

RUN pip install gunicorn pymysql cryptography

ENV FLASK_APP=microblog.py

RUN flask translate compile

RUN flask db upgrade

EXPOSE 5000

CMD ["gunicorn", "--bind", "0.0.0.0:5000", "-w", "4", "microblog:app"]
