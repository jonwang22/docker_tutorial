FROM python:latest

WORKDIR /app

COPY requirements.txt /app/

RUN pip install -r requirements.txt

RUN pip install gunicorn

COPY . /app

EXPOSE 8000

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "application:app"]
