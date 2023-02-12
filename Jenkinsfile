pipeline {
    agent {
        docker { image 'mrver0n/dockerwhitjenkins' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'docker image ls'
            }
        }
    }
}
/*node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("mrver0n/dockerwhitjenkins")

        /* Push the container to the custom Registry *//*
        customImage.push()
    }
}*/
