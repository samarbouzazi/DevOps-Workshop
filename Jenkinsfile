pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Send Email') {
            steps {
                script {
                    def readmeContent = readFile('README.txt')
                    emailext(
                        subject: "New Commit in my-project",
                        body: "A new commit has been made to the my-project repository. Check it out!\n\n${readmeContent}",
                        to: 'x@gmail.com'
                    )
                }
            }
        }
    }
}
