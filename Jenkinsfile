pipeline{
    agent any
    enviroment {
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
                bat "${env.PYHTON} extract.py"
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