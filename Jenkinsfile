pipeline {
    agent {
        docker {
            image 'node:gallium-bullseye-slim' 
            args '-p 4000:4000' 
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