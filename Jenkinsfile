pipeline {
    agent any
    stages { 
        stage('Building our image') { 
            steps { 
                script {
                  // CUSTOM REGISTRY
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {

                        /* Build the container image */
                        def dockerImage = docker.build("moonzkim/ai-service-fastapi:0.2.0")

                        /* Push the container to the custom Registry */
                        dockerImage.push()

                    }
               }
            } 
        }
    }
}
