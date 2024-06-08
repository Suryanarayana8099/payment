pipeline {
    agent any

    stages {
        stage('Checkout SCM') {
            steps {
                // Clone the Git repository
                git credentialsId: 'git', url: 'https://github.com/Suryanarayana8099/payment.git', branch: 'master'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t testing .'
                }
            }
        }
    }
}
