pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'dev',
                    credentialsId: 'github-pat',
                    url: 'https://github.com/ravindransamy/CICD.git'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                if not exist C:\\deploy mkdir C:\\deploy
                xcopy /E /Y index.html C:\\deploy
                '''
            }
        }
    }
}
