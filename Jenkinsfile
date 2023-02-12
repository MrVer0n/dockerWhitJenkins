pipeline {
    agent {
        docker { image 'mrver0n/dockerwhitjenkins' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
// Script //
node {
    /* Requires the Docker Pipeline plugin to be installed */
    docker.image('mrver0n/dockerwhitjenkins').inside {
        stage('Test') {
            sh 'node --version'
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
