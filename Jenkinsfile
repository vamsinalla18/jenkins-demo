pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'python3 -m pip install pytest'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
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