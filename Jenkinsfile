properties([pipelineTriggers([githubPush()])])
pipeline {
  agent any
  stages {
    stage('Checkout SCM') {
            steps {
                
                 git 'https://github.com/sureshguvva/sample-java-programs.git'
            }
    }
    
    stage('build') {
      steps {
        sh 'mvn -version'
        sh 'mvn clean install'
        }
    }
      stage('docker') {
        steps { 
        sh 'docker pull tomcat'
        }
      }
    }
   }
  
