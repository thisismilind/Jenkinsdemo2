pipeline{
    agent any

    environment {
        PYTHON = "C:\\Program Files\\Python310\\python.exe "

    }
    stages {
        stage('checkout code') {
            steps {
                checkout scm
            }

        }
        stage('Extract Data') {
            steps {
                bat "\"${env.PYTHON}\" extract_data.py "
            }
            
            
        }
    }
    post {
        success {
            echo "success..."

        }
        failure {
            echo "failure ..."

        }
        always {
            echo "always..."

        }
    }
}