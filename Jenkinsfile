pipeline {
    agent any

    tools {
        // Install the Maven tool globally available to the Jenkins instance
        maven 'Maven 3.8.4' // Adjust the Maven version as needed
    }

    stages {
        stage('Clone Repository') {
            steps {
                // Checkout the repository
                git url: 'https://github.com/Suryanarayana8099/user.git', branch: 'master'
            }
        }
        stage('Build') {
            steps {
                // Run Maven install
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Run Maven tests
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Example deploy step, you can replace this with your actual deploy commands
                echo 'Deploying...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
