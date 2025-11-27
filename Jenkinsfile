pipeline {
    agent {label 'VM'}
    stages{
        stage('SonarQube analysis') {
            steps{
                withSonarQubeEnv('SonarQube server') { // Will pick the global server connection you have configured
                    sh './gradlew sonar -Dhttp.proxyHost=proxy.corpnet.inside -Dhttp.proxyPort=8080 -Dhttps.proxyHost=proxy.corpnet.inside -Dhttps.proxyPort=8080'
                }
            }
        }
    }
}