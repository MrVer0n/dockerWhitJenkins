node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
        def customImage = docker.build("mrver0n/dockerwhitjenkins")  
        customImage.run('--name dockerwhitjenkins')
        //customImage.posh()
    }
}
