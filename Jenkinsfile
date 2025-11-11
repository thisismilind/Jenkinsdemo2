pipeline {
    agent any

    environment {
        PYTHON = "C:\\Program Files\\Python310\\python.exe"
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Extract Data') {
            steps {
                //  Correct quoting for Windows paths with spaces
                bat "\"${env.PYTHON}\" extract_data.py"
            }
        }
    }

    post {
        success {
            echo " success..."
        }
        failure {
            echo " failure..."
        }
        always {
            echo " always..."
        }
    }
}
