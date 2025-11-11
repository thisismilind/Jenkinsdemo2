pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/thisismilind/Jenkinsdemo2.git'
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code...'
                git url: "${GIT_REPO}", branch: 'main'
            }
        }

        stage('Extract Data') {
            steps {
                echo 'Running Extract Data step...'
                bat 'python extract_data.py'
            }
        }

        stage('Transform Data') {
            steps {
                echo 'Running Transform Data step...'
                bat 'python transform_data.py'
            }
        }

        stage('Load Data') {
            steps {
                echo 'Running Load Data step...'
                bat 'python load_data.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed.'
        }
        success {
            echo 'Pipeline succeeded!'
        }
    }
}
