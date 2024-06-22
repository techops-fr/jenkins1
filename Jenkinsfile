pipeline {
  agent any

  tools {
    grade "gradle8.9"
  }

  stages {
    stage('build') {
      steps {
        sh "gradle -v"
      }
    }
  }
}