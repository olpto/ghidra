pipeline {
    agent {label 'VM'}
    stages{
        stage('SonarQube analysis') {
            steps{
                withSonarQubeEnv('SonarQube server') { // Will pick the global server connection you have configured
                    sh './gradlew sonar'
                }
            }
        }
    }
}