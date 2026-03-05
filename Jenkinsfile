pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'docker build -t sre-app:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
            }
        }

    }
}
