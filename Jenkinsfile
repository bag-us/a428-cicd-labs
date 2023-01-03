pipeline {
    agent {
        docker {
            image 'node:lts-bullseye-slim' 
            args '-p 4040:4040' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}