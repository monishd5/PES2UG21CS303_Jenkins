pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
              build 'PES2UG21CS303-1'
              sh 'g++ -o main.cpp -o output'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
        }
        
        stage('Deploy'){
          steps {
            echo 'deploy'
          }
       }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
-
