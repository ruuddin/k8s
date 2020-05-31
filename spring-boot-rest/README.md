### Spring application

Build application: ./gradlew build

Start application:
 
    ./gradlew bootRun
    or
    java -jar build/libs/spring-boot-rest-0.0.1-SNAPSHOT.jar

Application will be running at port 9999: http://localhost:9999/api/rooms

### Package Java application as Docker image using Jib

1. Add plugin to build.gradle file
    id 'com.google.cloud.tools.jib' version '2.3.0'
2. Create gradle.properties and add USERNAME and PASSWORD for dockerhub. This file is ignored, do not checkin to GitHub.
3. Containerize the application: ./gradlew jib --image=<image>. This builds are pushes the image to registry.

### Kubernetes deployment
Look at the deployment and service manifest in spring-app-deployment.yaml
Run kubectl -n <ns> apply -f >yaml-file> to deploy the app
Go to http://<node>:30205/api/rooms to access the application
