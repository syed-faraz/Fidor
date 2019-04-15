pipeline {
  agent any
  tools {
    maven 'M3'
  }
  parameters {
    string(name: 'PipelineJob',
       defaultValue: 'maven',
       description: 'fidor solutions')
  } 
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}
