stage("Prepare container") {
  agent {
    docker {
      image 'openjdk:11.0.5-slim'
      args '-v $HOME/.m2:/root/.m2'
    }
  }
  stages {
    stage('Build') {
      steps {
        checkout scm
        sh './mvnw compile'
      }
    }
    stage('Test') {
      steps {
        sh './mvnw test'
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }
    stage('Package') {
      steps {
        sh './mvnw package -DskipTests'
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
