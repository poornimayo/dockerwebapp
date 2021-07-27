node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'dockerHub') {

        def customImage = docker.build("poornimayo98/dockerwebapp")

        /* Push the container to the custom Registry */
        customImage.push("${env.BUILD_NUMBER}")
        customImage.push("lastest")
    }
}
