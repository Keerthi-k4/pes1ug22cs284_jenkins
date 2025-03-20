pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ fail fail -o main/hello_exec main/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './main/hello_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application (Placeholder)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
