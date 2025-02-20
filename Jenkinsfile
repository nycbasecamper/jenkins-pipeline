// Reference the shared library by its name
@Library('BCS_CES_bcs-shared-library') _  // Load the shared library

pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm  // Checkout the code from your repository
            }
        }

        stage('Say Hello') {
            steps {
                script {
                    // Call the sayHello function from the shared library
                    sayHello()  // This will invoke the sayHello.groovy script
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Add your build steps here
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
