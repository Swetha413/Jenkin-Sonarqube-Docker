pipeline {
    agent any
    tools {
        sonarQube 'SonarQube Scanner installations'
    }
    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'sonar-scanner'
                }
            }
        }
    }
}
