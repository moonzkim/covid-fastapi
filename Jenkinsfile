pipeline {
    agent {
        kubernetes {
            defaultContainer 'jnlp'
            yamlFile 'agentpod.yaml'
        }
    }
    stages { 
        stage('Building image') { 
            steps { 
                container('docker') {
                
                
                    sh "docker build . -t moonzkim/ai-service-fastapi:0.2.0"
                    sh "docker images" 
                
                }
            } 
        }
    }
}
    
