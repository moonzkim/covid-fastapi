pipeline {
    agent any
    stages { 
        stage('Building our image') { 
            steps { 
                script {
                  // CUSTOM REGISTRY
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

                        /* Build the container image */
                        def dockerImage = docker.build("moonzkim/ai-service-fastapi:$BUILD_ID")

                        /* Push the container to the custom Registry */
                        dockerImage.push()

                    }
               }
            } 
        }
    }
}
