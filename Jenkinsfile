pipeline {
    agent any

    environment {
        scannerHome = tool 'SonarScanner' // Match with Jenkins config
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Swetha413/Jenkin-Sonarqube-Docker.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    withCredentials([string(credentialsId: 'sonarqube-token-2025', variable: 'SONAR_TOKEN')]) {
                        sh """
                            ${scannerHome}/bin/sonar-scanner \\
                              -Dsonar.login=$SONAR_TOKEN
                        """
                    }
                }
            }
        }
    }
}
