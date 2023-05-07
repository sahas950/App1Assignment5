pipeline {
    agent any
    triggers {
        pollSCM('*/5 * * * *')
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp target/myapp.war $CATALINA_HOME/webapps'
            }
        }
    }
}


