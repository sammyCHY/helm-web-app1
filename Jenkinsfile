pipeline {
    agent any

    environment {
        HELM = 'C:\\ProgramData\\chocolatey\\bin\\helm.exe'
    }



        stage('Deploy with Helm') {
            steps {
                bat "\"%HELM%\" upgrade --install my-webapp ./webapp --namespace default"
            }
        }
    }
