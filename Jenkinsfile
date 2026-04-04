pipeline {
    agent any

    environment {
        HELM = 'C:\\ProgramData\\chocolatey\\bin\\helm.exe'
    }

    stages {
        stage('Test Kubernetes') {
            steps {
                bat 'kubectl get nodes'
            }
        }

        stage('Deploy with Helm') {
            steps {
                bat "\"%HELM%\" upgrade --install my-webapp ./webapp --namespace default"
            }
        }
    }
}