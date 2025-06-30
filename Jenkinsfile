pipeline {
    agent any

    environment {
        scannerHome = tool 'SonarScanner' // This name must match what you configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Swetha413/Jenkin-Sonarqube-Docker.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') { // This must match the name of your SonarQube server in Jenkins config
                    sh "${scannerHome}/bin/sonar-scanner"
                }
            }
        }
    }
}

