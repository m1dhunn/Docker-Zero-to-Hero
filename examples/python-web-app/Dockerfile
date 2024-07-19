FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

RUN sudo apt-get update && \
    sudo apt-get install -y python3 python3-pip python3-venv && \
    python3 -m venv devops_env && \
    source devops_env/bin/activate && \
    pip install -r requirements.txt && \
    cd devops


ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




