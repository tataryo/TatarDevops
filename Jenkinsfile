pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from GitHub
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Clean and package using Maven (optional)
                sh 'mvn clean package'
                // You can replace 'mvn clean package' with your specific build commands
            }
        }
    }

    // Post-build actions (e.g., notifications)
    post {
        success {
            echo 'Build successful! Implement your post-build actions here.'
        }
        failure {
            echo 'Build failed! Implement your post-failure actions here.'
        }
    }
}
