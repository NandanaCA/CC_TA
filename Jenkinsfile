pipeline {
    agent any  

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ PES2UG22CS336.cpp -o PES2UG22CS336' 
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS336' 
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
            echo 'Pipeline failed'  
        }
    }
}
