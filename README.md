# docker-ubuntu1604-swarm

build & start
```
docker network create swarm_shared
docker-compose up --force-recreate --build -d
```

login(password: root)
```
ssh root@localhost -p 221
```

sworm
```
cd work/demoS
mvn clean package && java -jar target/demo-thorntail.jar -Djava.net.preferIPv4Stack=true
```

access
```
http://localhost:221/hello
```

stop
```
docker-compose down
```

## all stop & remove  
docker stop $(docker ps -q)  
docker rm $(docker ps -q -a)  
docker rmi $(docker images -q)  

## if"WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED! " appears
Delete the line of the corresponding host from "known_hosts".