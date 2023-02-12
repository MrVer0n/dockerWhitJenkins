node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("mrver0n/dockerwhitjenkins")
        /* Push the container to the custom Registry */
        //customImage.push()
    }
}

pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'docker run -p 49160:8080 -d mrver0n/dockerwhitjenkins'
            }
        }
    }
}
