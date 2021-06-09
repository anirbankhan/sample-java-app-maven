@Library('my-shared-library@1.0') _
pipeline {
    agent any
        tools {
            maven 'Maven 3.8.1'
            jdk 'jdk-1.8.0_275'
        }
        stages {
            stage('Demo') {
                echo "Hello World!"
                sayHello "Anirban"
            }
            stage('Build') {
                steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install'
                }
        }
    }
}
