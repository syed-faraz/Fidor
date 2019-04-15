pipeline {
  agent any
  tools {
    maven 'apache-maven-3.6.1'
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
