pipeline {
  agent {
    kubernetes {
      yaml """
apiVersion: v1
kind: Pod
metadata:
  labels:
    name: remote-agent
spec:
  containers:
  - name: kaniko
    image: gcr.io/kaniko-project/executor:debug
    imagePullPolicy: Always
    command:
    - /busybox/cat
    tty: true
    env:
    - name: GOOGLE_APPLICATION_CREDENTIALS
      value: "/kaniko/config.json"
"""      
    }
  }
  stages {
    stage('Build & Push') {
      steps {
        container(name: 'kaniko', shell: '/busybox/sh') {
          }
        
      }
    }
  }
}