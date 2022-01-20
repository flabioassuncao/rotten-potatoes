FROM python:3.8-slim-buster
WORKDIR /app
COPY requirements.txt .
RUN python -m pip install -r requirements.txt
COPY . /app
EXPOSE 5000
CMD ["gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "-c", "config.py", "app:app"]
# docker build -t flabioassuncao/rotten-potatoes:v1 .
# k3d cluster create meucluster --agents 3 --servers 3 -p "8080:30000@loadbalancer"
# kubectl apply -f deployment.yaml  