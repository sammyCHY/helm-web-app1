ppipeline {
    agent any

    environment {
        HELM = 'C:\\ProgramData\\chocolatey\\bin\\helm.exe'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/sammyCHY/helm-web-app1.git'
            }
        }

        stage('Deploy with Helm') {
            steps {
                bat "\"%HELM%\" upgrade --install my-webapp ./webapp --namespace default"
            }
        }
    }
}