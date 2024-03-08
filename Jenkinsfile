pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Your build commands here
                    echo 'Building...'
                    sh 'make'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Your test commands here
                    echo 'Testing...'
                    sh 'make test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Your deployment commands here
                    echo 'Deploying...'
                    sh 'make deploy'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
