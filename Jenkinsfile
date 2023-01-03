pipeline {
    agent {
        docker {
                image 'node:gallium-bullseye-slim'
                args '-p 3000:3000' 
            }
        }
    stages {
        stage('Build') {
            steps {
                sh 'nmp config set legacy-peer-deps true'
                sh 'npm install'
            }
        }
    }
}