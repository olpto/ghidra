pipeline {
    agent {label 'VM'}
    stages{
        stage('SCM') {
            steps{
                checkout scm
            }
        }
        stage('SonarQube analysis') {
            steps{
                withSonarQubeEnv('SonarQube server') { // Will pick the global server connection you have configured
                    sh './gradlew sonar'
                }
            }
        }
    }
}