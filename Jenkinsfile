pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo "build success"
            }
        }
         stage('Send Email') {
            steps {
                script {
                    def readmeContent = readFile('README.txt')
                    mail bcc: '', body: '{readmeContent}', cc: '', from: '', replyTo: '', subject: 'README', to: 'samar.bouzezi@esprit.tn'
                }
            }
        }
    }
    
}
