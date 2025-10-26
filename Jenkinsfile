pipeline {
    agent any
  
    stages {
        stage("restore .NET Packages") {
            steps {
                bat 'dotnet restore'
            }
        }

        stage("Build .NET Project") {
            steps {
                bat 'dotnet build --no-restore'
            }
        }

        stage("Run Unit and Integration Tests") {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
