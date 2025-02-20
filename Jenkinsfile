// Reference the shared library by its name
@Library('bcs-shared-library') _  // Load the shared library

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from the repository...'
                checkout scm  // Checkout the code from your repository
            }
        }

        stage('Say Hello') {
            steps {
                script {
                    echo 'Calling the sayHello function from the shared library...'
                    sayHello()  // This will invoke the sayHello.groovy script
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                standardPipelineCI()
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here
            }
        }
    }
}
