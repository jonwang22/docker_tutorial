FROM python

EXPOSE 8000

RUN git clone https://github.com/kura-labs-org/c4_deployment-4.git

WORKDIR c4_deployment-4

RUN pip install -r requirements.txt

RUN pip install gunicorn

ENTRYPOINT ["python3", "-m", "gunicorn", "-w", "4", "application:app", "-b", "0.0.0.0"]

