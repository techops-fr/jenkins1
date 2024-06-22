pipeline {
  agent any

  tools {
    gradle "gradle8.9"
  }

  stages {
    stage('build') {
      steps {
        sh "gradle -v"
      }
    }
  }
}