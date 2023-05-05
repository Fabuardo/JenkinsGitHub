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
    }
        post {
            failure {
                slackSend(channel: '#fundamentos-de-devops', message: ' Estimado Fabián T, su ppeline no se ejecutó, revise la configuración')
            }
            success {
                slackSend(channel: '#fundamentos-de-devops', message: ' Estimado Fabián T., su pipeline se ejecutó correctamente :smile: ...')
            }
        }
    }

