pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                  build 'PES2UG23CS809-1'
                    sh 'g++ -o output PES2UG23CS809-1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Run the compiled binary
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
