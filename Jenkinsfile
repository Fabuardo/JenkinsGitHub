// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        post {
            failure {
                slackSend(channel: '#fundamentos-de-devops', message: ' Falló la ejecución')
            }
            success {
                slackSend(channel: '#fundamentos-de-devops', message: ' Se ejecutó correctamente')
            }
        }
    }
}
