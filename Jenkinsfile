pipeline {
    agent any
    stages {
        stage('Restore .NET Packages') {
            steps {
                bat 'dotnet restore' //For Windows
            }
        }
        stage('Build .NET Project'){
            steps {
                bat 'dotnet build --no-restore' //For Windows
            }
        }
        stage('Run Unit and Integrations Tests'){
            steps {
                bat 'dotnet test --no-build --verbosity normal' //For Windows
            }
        }
    }
    
}