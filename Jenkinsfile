pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS069-1'
                sh 'g++ working.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                // Your deploy steps go here
                echo 'Deploying..'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
