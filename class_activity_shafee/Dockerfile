FROM python:3.7

EXPOSE 5000

RUN git clone https://github.com/kura-labs-org/C5-Deployment-Workload-2.git

WORKDIR C5-Deployment-Workload-2

RUN pip install -r requirements.txt

ENTRYPOINT ["python3.7", "application.py"]

