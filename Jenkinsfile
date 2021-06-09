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
                evenOrAdd(currentBuild.number)
                }
            }
            
            stage('Build') {
                agent any
                steps {
                    shell 'mvn -Dmaven.test.failure.ignore=true install'    
                }
        }
    }
}
