pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run tests using Maven (assuming JUnit is configured in your project)
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Add deployment steps here if needed
                echo 'Deployment steps go here...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline successful! Ready for production deployment.'
        }
        failure {
            echo 'Pipeline failed! Please check the build logs for errors.'
        }
    }
}
