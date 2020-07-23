node {

 
stage('init') {

 
checkout scm

 
}

 
stage('build' {

 
sh '''
 
mvn clean package
 
'''

 
}

 
stage('Build image') {

 
app = docker.build("venkyroyal121/beat")

 
}

 
 

 
stage('push image') {

 
docker.withRegistry('https://registry.hub.docker.com', 'DOCKERHUB VENKY') {

 
app.push("latest")

 
}

 
echo "trying to docker image to docker hub"

 
}
 
 stage('sonarqube') {
 sh '''
 mvn clean package sonar:sonar
 '''
 }
 
}
