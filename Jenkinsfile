pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t my_node_app .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run --rm my_node_app npm test'
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/deployment.yaml'
                sh 'kubectl apply -f k8s/service.yaml'
            }
        }
    }
}
