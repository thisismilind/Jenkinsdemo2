pipeline{
    agent any
    
    environment {
        PYTHON = "C:\\Program Files\\Python310\\python.exe "

    }
    stages {
        stage('checkout code') {
            steps {
                checkout code
            }

        }
        stage('Extract Data') {
            steps {
                bat "${env.PYHTON} extract_data.py"
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