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

        stage('Deploy and Open Dashboard') {
            steps {
                 '''
                    Start-Process powershell -ArgumentList "-ExecutionPolicy Bypass -File .\\run_project.ps1"
                    Start-Sleep -Seconds 5
                    Start-Process "http://localhost:3000"
                '''
            }
        }
    }
}
