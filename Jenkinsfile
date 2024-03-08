pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Your build commands here
                    sh 'g++ -o executable main/hello.cpp'

                }
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                script {
                    // Your test commands here
                   
                    sh './executable'

                }
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Your deployment commands here
                    echo 'Deployment successful'
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
