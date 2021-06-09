@Library('my-shared-library') _
pipeline {
    agent any
        tools {
            maven 'Maven 3.8.1'
            jdk 'jdk-1.8.0_275'
        }
        stages {
            stage('Demo') {
                steps {
                echo "Hello World!"
                sayHello "Anirban"
                script {
                nexus_url=evenOrAdd(2)
                echo $nexus_url
                }
                }
            }
            
            stage('Build') {
                steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install'
                }
        }
    }
}
