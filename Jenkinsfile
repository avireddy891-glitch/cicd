pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Home Automation Project'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Home Automation Project'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                start "HomeAutomationServer" cmd /c "cd /d %WORKSPACE%\\frontend && python -m http.server 8000"
                '''
                echo 'Dashboard deployed at http://localhost:8000'
            }
        }
    }

    post {
        success {
            echo 'CI/CD completed successfully!'
            echo 'Open dashboard: http://localhost:8000'
        }
    }
}
