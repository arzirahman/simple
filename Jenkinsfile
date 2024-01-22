pipeline {
    agent any

    stages {
        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('SonarQube') {
                    sh 'mvn clean install'
                    sh 'mvn clean verify sonar:sonar'
                    echo 'SonarQube Analysis Completed'
                }
            }
        }
    }
}