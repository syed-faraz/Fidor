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
      steps {
        sh "echo Hello ${params.description}, your ${params.defaultValue} ${params.name} is successful"
      }  
      }
    }
  }
}
