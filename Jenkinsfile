pipeline {
    agent any
        tools {
            nodejs '18.12.1'  
        }
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}