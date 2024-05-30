# traefik-swarm
docker login 127.0.0.1:8082

docker build -t traefik-test:latest .
docker tag traefik-test:latest 10.211.55.13:8082/repository/docker-hosted/traefik-test:latest
docker push 10.211.55.13:8082/repository/docker-hosted/traefik-test:latest
docker stack deploy -c docker-compose.yml --with-registry-auth traefik