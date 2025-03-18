pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Intentional error: Using an invalid command
                sh 'invalid_command_here'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
// pipeline {
//     agent any
//     stages {
//         stage('Build') {
//             steps {
//                 sh 'g++ -o hello_exec main/hello.cpp'
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh './hello_exec'
//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'Deployment Stage: Not Implemented'
//             }
//         }
//     }
//     post {
//         failure {
//             echo 'Pipeline failed!'
//         }
//     }
// }
