node {

 
stage('init') {

 
checkout scm

 
}

 
stage('build') {

 
sh '''
 
mvn clean package
 
'''

 
}

 
stage('Build image') {

 
app = docker.build("venkyroyal121/BEAT")

 
}

 
 

 
stage('push image') {

 
docker.withRegistry('https://registry.hub.docker.com', 'DOCKERHUB2') {

 
app.push("latest")

 
}

 
echo "trying to docker image to docker hub"

 
}

 
 

 
}
