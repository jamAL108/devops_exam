pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/jamAL108/devops_exam.git'
            }
        }


        stage('Deploy to XAMPP') {
            steps {
                // Copy the HTML files to XAMPP htdocs directory
                bat 'xcopy /E /Y .\\*.html "C:\\xampp\\htdocs\\"'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
