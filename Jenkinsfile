pipeline {
  agent any
  tools {
    maven 'M3'
  }
  
  parameters {
    string(name: 'PipelineJob',
       defaultValue: 'maven',
       description: 'Fidor Solutions')
  } 
  
  #options([pipelineTriggers([pollSCM('H * * * *')])])
  
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
        post {
          success {
            sh "echo your '${params.PipelineJob}' job is successful"
          }  
        }
      }
    }  
    stage('deploy') {
      steps {
        sh 'mvn deploy'
      }
    }  
  }
 
}
