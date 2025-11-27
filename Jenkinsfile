pipeline {
    agent {label 'VM'}
    stages{
        stage('SonarQube analysis') {
            steps{
                withSonarQubeEnv('SonarQube server') { // Will pick the global server connection you have configured
                    sh './gradlew sonar -Dhttp.proxyHost=127.0.0.1 -Dhttp.proxyPort=3128 -Dhttps.proxyHost=127.0.0.1 -Dhttps.proxyPort=3129'
                }
            }
        }
    }
}