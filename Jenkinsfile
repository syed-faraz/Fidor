pipeline {
  agent any
  parameters {
    string(name: 'PipelineJob',
       defaultValue: 'maven',
       description: 'fidor solutions')
  } 
  stages {
    stage('compile') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
