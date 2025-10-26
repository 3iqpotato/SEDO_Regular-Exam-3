pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')  // Проверява за промени на всеки 5 минути
    }

    stages {
        stage('Build') {
            steps {
                sh 'dotnet build --configuration Release'
            }
        }

        stage('Test') {
            steps {
                sh 'dotnet test --no-build --configuration Release'
            }
        }
    }
}
