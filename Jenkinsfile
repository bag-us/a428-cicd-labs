pipeline {
    agent {
        docker {
            args '-p 4040:4040' 
            tools {
                nodejs '18.12.1' 
            }
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