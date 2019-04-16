pipeline {
  agent any
  triggers { 
    pollSCM('H/5 * * * *') 
  }
  tools {
    maven 'M3'
  }
  
  parameters {
    string(name: 'PipelineJob',
       defaultValue: 'maven',
       description: 'Fidor Solutions')
  } 
  
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
      }
    }
    
    stage('deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
  }  
        
  post {
    success {
      sh "echo your '${params.PipelineJob}' job is successful"
    }  
  }
 
}
