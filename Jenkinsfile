pipeline {
    agent any

 

    stages {
        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }
        stage('Build Image') {
            steps {
                sh 'sudo docker build -t myflaskimage:v1 .'
            }
        }
        stage('Run Image') {
            steps {
                sh 'sudo docker run -d -p 5000:5000 myflaskimage:v1'

            }

        }
        stage('Testing') {
            steps {
               echo 'Testing'
            }
        }
    }
}