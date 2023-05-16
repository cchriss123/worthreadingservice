# Worthreadingservice

The Worth Reading Service is a Java-based microservice managing the liking functionality for messages. \
It is a part of a larger application and provides RESTful APIs to handle likes on messages.

### Runs on port 8005 with with a MYSQL database on port 3306.

## Native compile
- export JAVA_HOME=/Library/Java/JavaVirtualMachines/graalvm-ce-java17-22.3.1/Contents/Home 
- mvn clean package -Pnative native:compile -DskipTests

## JVM compile 
- mvn clean package 

### Run docker compose to build application and database in container

## API Endpoints

#### Toggle Like: 
- PUT /like/toggleLike/{messageId}

#### Bulk Check: 
- GET /like/bulkIsLiked

#### Is Liked: 
- GET /like/isLiked/{messageId}/{userId}
 
#### Get Likes: 
- GET /like/amount/{messageId}

#### Users who Liked: 
- GET /like/users/{messageId}

## Download docker image
#### Native arm64 native image:
-docker pull cchriss123/worthreadingservice:1.0.0

#### Regular JVM version image
- docker pull ghcr.io/chatgut/worthreadingservice:latest


