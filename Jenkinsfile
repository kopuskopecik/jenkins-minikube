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
                bat 'helm install -f C:/Users/User/Desktop/Demo/mychart/values.yaml  myhelm C:/Users/User/Desktop/Demo/mychart/'
            }
        }
    }
}
