pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS097-1'
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
                cho 'Deploying..'
            }
        }
    }

    post {
        failure {
            echo 'pipeline failed'
        }
    }
}
