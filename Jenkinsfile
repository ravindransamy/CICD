pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'dev',
                    credentialsId: 'github-pat',
                    url: 'https://github.com/ravindransamy/CICD.git'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                mkdir -p /var/jenkins_home/deploy
                cp index.html /var/jenkins_home/deploy/
                '''
            }
        }
    }
}
