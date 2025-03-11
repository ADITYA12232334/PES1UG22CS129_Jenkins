pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG22CS129.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                        sh './nonexistent_executable' // Intentional error
                }
            }
        }


        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed ❌'
        }
    }
}
