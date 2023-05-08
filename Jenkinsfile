pipeline {
    agent any
    triggers {
        pollSCM('*/5 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                powershell 'mvn clean install'
            }
        }
        stage('Deploy') {
            steps {
                powershell 'cp target/App1Assignment5.war $CATALINA_HOME/webapps'
            }
        }
    }
}


