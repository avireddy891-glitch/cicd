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
        bat '''
        start "" powershell -NoProfile -ExecutionPolicy Bypass -File ".\\run_project.ps1"
     powershell -NoProfile -Command "Start-Sleep -Seconds 10"
        start "" "http://localhost:3000"
        '''
            }
        }
    }
}
