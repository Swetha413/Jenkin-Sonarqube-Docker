pipeline {
    agent any

    environment {
<<<<<<< HEAD
        scannerHome = tool 'SonarScanner' // Match with Jenkins config
=======
        scannerHome = tool 'SonarScanner' // This name must match what you configured in Jenkins
>>>>>>> aa7e7bbbbe6b3a2d5324b70844b951a1507b61c0
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Swetha413/Jenkin-Sonarqube-Docker.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
<<<<<<< HEAD
                withSonarQubeEnv('SonarQube') {
                    withCredentials([string(credentialsId: 'sonarqube-token-2025', variable: 'SONAR_TOKEN')]) {
                        sh """
                            ${scannerHome}/bin/sonar-scanner \\
                              -Dsonar.login=$SONAR_TOKEN
                        """
                    }
=======
                withSonarQubeEnv('SonarQube') { // This must match the name of your SonarQube server in Jenkins config
                    sh "${scannerHome}/bin/sonar-scanner"
>>>>>>> aa7e7bbbbe6b3a2d5324b70844b951a1507b61c0
                }
            }
        }
    }
}
<<<<<<< HEAD
=======

>>>>>>> aa7e7bbbbe6b3a2d5324b70844b951a1507b61c0
