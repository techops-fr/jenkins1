pipeline {
  agent any

  stages {
    stage('Build and test') {
      matrix {
        axes {
          axis {
            name 'PLATFORM'
            values 'linux', 'macos', 'windows'
          }
          axis {
            name 'BROWSER'
            values 'firefox', 'chrome', 'safari'
          }
        }
        stages {
          stage('Build'){
            steps {
              echo "Etape de build pour ${BROWSER} sur ${PLATFORM}"
            }
          }
          stage('Tests'){
            steps {
              echo "Etape de test pour ${BROWSER} sur ${PLATFORM}"
            }
          }
        }
      }
    }
  }
}