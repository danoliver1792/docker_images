FROM python:3

RUN apt-get update -y && \
    apt-get install -y python-pip python-dev

WORKDIR /app

RUN pip install Flask

COPY . .

EXPOSE 5000

CMD ["python", "./app.py"]

# no terminal
# docker build -t danoliver1792/flask-kub-projeto .
# docker run -d -p 5000:5000 --name flask-kub --rm danoliver1792

# docker container ls
# docker push danoliver1792/flask-kub-projeto


# no Kubernetes, criando o deployment para rodas os containers das aplicações nos pods

# kubectl create deployment flask-deployment --danoliver1792/flask-kub-projeto

# minikube service flask-deployment

# atualizando a imagem
# docker build -t danoliver1792/flask-hub-projeto:2 .
# docker push danoliver1792/flask-kub-orjeto:2
# kubectl set image deployment/flask-deployment flask-projeto=danoliver1792/flask-kub-projeto:2
# kubectl get deplyments
# kubectl get pods
