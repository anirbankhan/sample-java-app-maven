@Library('my-shared-library') _
pipeline {
    agent any
        tools {
            maven 'Maven 3.8.1'
            jdk 'jdk-1.8.0_275'
        }
        parameters {
            choice(name:'Environment', choices:['SIT','SVT'],description:'Pick Env for comparison')
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
                    sh 'mvn -Dmaven.test.failure.ignore=true install'    
                }
            }
            stage('Test') {
                steps {
                    script {
                        if (params.ENVIRONMENT="SIT"||params.ENVIRONMENT="SVT")
                        {
                            echo params.ENVIRONMENT
                        }
                    }
                }
            } 
    }
}
