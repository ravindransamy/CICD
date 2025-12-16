pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying files to C:\\deploy'
                bat '''
                if not exist C:\\deploy mkdir C:\\deploy
                xcopy /E /Y /I *.html C:\\deploy
                '''
            }
        }
    }
}
