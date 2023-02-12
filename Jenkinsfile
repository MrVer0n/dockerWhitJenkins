node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

        def customImage = docker.build("mrver0n/dockerwhitjenkins")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}
