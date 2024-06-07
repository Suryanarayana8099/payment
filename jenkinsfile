pipeline {
    agent any
    
    stages {
        stage('SCM Checkout') {
            steps {
                // Checkout the source code from the specified public Git repository
                git branch: 'main', url: 'https://github.com/Suryanarayana8099/catalogue'
            }
        }
    }
}
