pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/sammyCHY/helm-web-app1.git'
            }
        }

        stage('Deploy with Helm') {
            steps {
                script {
                    sh '/usr/local/bin/helm upgrade --install my-webapp ./webapp --namespace default'
                }
            }
        }
    }
}