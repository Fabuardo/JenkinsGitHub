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
            always {
                slackSend(channel: '#fundamentos-de-devops', message: ' Estimado Fabián T, su pipeline se esta ejecutando, se le avisará si se ejecutó correctamente o no')
            }
            failure {
                slackSend(channel: '#fundamentos-de-devops', message: ' :fire: Estimado Fabián T, su ppeline no se ejecutó, revise la configuración :fire:')
            }
            success {
                slackSend(channel: '#fundamentos-de-devops', message: ' Estimado Fabián T., su pipeline se ejecutó correctamente :smile: ...')
            }
        }
    }

