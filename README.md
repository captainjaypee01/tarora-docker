## Create Password for mosquitto

mkdir -Force .\infra\mosquitto\ | Out-Null
docker run --rm -it `  -v ${PWD}\infra\mosquitto:/mosquitto `  eclipse-mosquitto:2 `  mosquitto_passwd -c /mosquitto/passwd tarora    

## Docker commands

### build
docker compose --profile api build --no-cache api
docker compose --profile sim build 

### run container
docker compose --profile api --profile sim up

### Dockerfiles
Create Docker files