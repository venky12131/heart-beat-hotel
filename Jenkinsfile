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

 
app = docker.build("venkyroyal121/heartbeat")

 
}

 
 

 
stage('push image') {

 
docker.withRegistry('https://registry.hub.docker.com', 'doc') {

 
app.push("latest")

 
}

 
echo "trying to docker image to docker hub"

 
}

 
 

 
}
