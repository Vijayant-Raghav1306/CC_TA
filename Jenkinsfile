pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile .cpp file using g++ and make
                    sh 'g++ main/hello.cpp -o main/hello_exec'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Print the output of the .cpp file
                    shi './main/hello_exec'
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy stage - Add your deploy steps here'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
