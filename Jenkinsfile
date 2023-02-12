pipeline {
    agent none
    stages {
        stage('Front-end') {
            agent {
                docker { image 'mrver0n/dockerwhitjenkins:tagname' }
            }
            steps {
                sh 'node --version'
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
