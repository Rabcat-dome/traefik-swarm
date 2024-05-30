# traefik-swarm
docker build -t traefik-test:latest .
docker tag traefik-test:latest 127.0.0.1:8082/repository/docker-hosted/traefik-test:latest

docker login 127.0.0.1:8082
docker push 127.0.0.1:8082/repository/docker-hosted/traefik-test:latest