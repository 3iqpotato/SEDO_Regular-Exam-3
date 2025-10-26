pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')   // проверява за промени на всеки 5 минути
    }

    stages {
        stage('Build') {
            steps {
                bat 'dotnet build --configuration Release'
            }
        }

        stage('Test') {
            steps {
                bat 'dotnet test --no-build --configuration Release'
            }
        }
    }
}
