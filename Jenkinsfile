pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat "docker build -t erdogansahin/hello:latest ."
            }
        }
        stage('Push') {
            steps {
                bat "docker push erdogansahin/hello:latest"
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f C:/Users/User/Desktop/Demo --context minikube'
            }
        }
    }
}
