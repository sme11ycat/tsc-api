# tsc-api

### 1. build jar:
mvn clean build -Dmaven.test.skip=true

### 2. build image:
docker build --build-arg JAR_FILE=target/*.jar -t ikigai-team/tsc-api .

### 3. run:
docker run -p 1024:1024 -e SPRING_PROFILE=local ikigai-team/tsc-api

### Check it:
http://localhost:1024/tsc/api/actuator/health
http://localhost:1024/tsc/api/swagger-ui/index.html