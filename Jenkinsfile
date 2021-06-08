pipeline {
    agent any
        tools {
            maven 'Maven 3.8.1'
            jdk 'jdk-1.8.0_275'
        }
        stages {
            stage('Build') {
                steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install'
                }
        }
    }
}
