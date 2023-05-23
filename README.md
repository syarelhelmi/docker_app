# docker_app

1. Create a new directory :

mkdir Assignment
cd Assignment

2. Create Dockerfile
vim Dockerfile

```FROM nginx:latest

```COPY . /usr/share/nginx/html

```EXPOSE 80

```CMD ["nginx", "-g", "daemon off;"]


3. Create a docker-compose.yml
vim docker-compose.yml

```services:
```web:
```    build:
```    context: .
```    dockerfile: Dockerfile
```    ports:
```    - '8080:80'
```    volumes:
```    - .:/usr/share/nginx/html
```    deploy:
```    resources:
```        limits:
```        cpus: '0.5'
```        memory: '512M'

4.Create html : index.html



5. Website - ipaddress:8080






 


