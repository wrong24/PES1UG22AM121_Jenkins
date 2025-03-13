pipeline {
    agent any

    environment {
        FILE_NAME = 'main.cpp'
        BUILD_NAME = 'pes1ug22am121-1'
    }

    stages {
        stage('Build') {
            steps {
                scriptsss {
                    sh 'g++ ${FILE_NAME} -o ${BUILD_NAME}'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './${BUILD_NAME}'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
