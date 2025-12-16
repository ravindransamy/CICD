pipeline {
    agent any

    stages {
        stage('Test Echo') {
            steps {
                echo 'HELLO FROM JENKINS PIPELINE'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                echo Deploying...
                if not exist C:\\deploy mkdir C:\\deploy
                echo Jenkins was here > C:\\deploy\\jenkins.txt
                '''
            }
        }
    }
}
