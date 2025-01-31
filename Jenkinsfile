pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Rebuilding the image locally
                    sh 'docker build -t my-k8s-app .'
                }
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    // Applying deployment and service
                    sh 'kubectl apply -f kubernetes/deployment.yaml'
                    sh 'kubectl apply -f kubernetes/service.yaml'
                }
            }
        }
    }
}
