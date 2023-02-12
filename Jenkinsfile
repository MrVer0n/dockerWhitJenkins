node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("mrver0n/dockerwhitjenkins")
        customImage.withRun() {}
        /* Push the container to the custom Registry */
        //customImage.push()
    }
}

/*pipeline {
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
}*/
