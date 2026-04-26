pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    environment {
        KUBECONFIG = '/var/lib/jenkins/.kube/config'
        HELM = '/usr/local/bin/helm'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/sammyCHY/helm-web-app1.git'
            }
        }

        stage('Deploy with Helm') {
            steps {
                sh '''
                    kubectl get nodes
                    helm upgrade --install my-webapp ./webapp --namespace default
                '''
            }
        }
    }
}