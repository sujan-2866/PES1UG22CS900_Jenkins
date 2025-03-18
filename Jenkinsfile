pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello_exec main/hello.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Stage: Not Implemented'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
