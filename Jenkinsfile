pipeline {
    agent any
    
    stages {
        stage('Restore') {
            steps {
                // Restore the project dependencies
                sh 'dotnet restore'
            }
        }
        
        stage('Build') {
            steps {
                // Build the .NET project
                sh 'dotnet build'
            }
        }
        
        stage('Test') {
            steps {
                // Run the tests
                sh 'dotnet test'
            }
        }
        
        stage('Publish') {
            steps {
                // Publish the application
                sh 'dotnet publish -c Release -o ./publish'
            }
        }
    }
}
