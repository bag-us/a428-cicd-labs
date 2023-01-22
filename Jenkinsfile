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
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
        stage('Manual Approve'){
            steps{
                input message: 'Lanjutkan ke tahap Deploy? (Klik "Proceed" untuk melanjutkan eksekusi)'
            }
        }
        stage('Deploy') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                sh './jenkins/scripts/kill.sh'
            }
            post {
                success {
                    echo "Tunggu sesaat, aplikasi sedang di Deploy"
                    sh 'sleep 60'
                }
            }
        }
    }
}