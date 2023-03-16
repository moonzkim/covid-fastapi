pipeline {
    agent any
    stages { 
        stage('Building our image') { 
            steps { 
                script { 
                    sh "service docker start"
                    sh "./docker/docker build . -t moonzkim/ai-service-fastapi:0.2.0"
                    sh "./docker/docker images" 
                }
            } 
        }
    }
}
    
