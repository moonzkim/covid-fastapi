pipeline {
    agent any
    stages { 
        stage('Building our image') { 
            steps { 
                script { 
		    sh "ls"
                    sh "docker build . -t moonzkim/ai-service-fastapi:0.2.0"
                    sh "docker images" 
                }
            } 
        }
    }
}
