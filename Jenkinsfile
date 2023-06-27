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
                bat 'kubectl apply -f deployment.yaml --cluster minikube'
            }
        }
    }
}
