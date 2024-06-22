pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh 'echo hello > world.txt'
        archiveArtifacts(artifacts: "**/*.txt") // Tous les *.txt, même sous répertoires
      }
    }
  }
}