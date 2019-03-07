node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t docker_test:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'mikodongo' -p 'Mqxzygi4%iaj' "
sh "docker tag docker_test:latest mikodongo/test3:latest"
sh "docker push mikodongo/test3:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
