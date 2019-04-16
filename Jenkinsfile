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
  
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
      }
    }
  }  
        
  post {
    success {
      sh "echo your '${params.PipelineJob}' job is successful"
    }  
  }
 
}
