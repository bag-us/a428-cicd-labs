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
                // sh 'npm install --force'
                // sh 'npm install --legacy-peer-deps'
                sh 'npm install'
            }
        }
        // stage('Test') {
        //     steps {
        //         sh './jenkins/scripts/test.sh'
        //     }
        // }
    }
}