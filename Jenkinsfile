pipeline {
  agent any

  triggers {
    cron("*/2 * * * *") // Déclenchement du pipeline toutes les 2 minutes
  }

  stages {
    stage('build') {
      options {
        timestamps()
      }
      steps {
        echo "Build!"
      }
    }
  }

  post {
    always {
      echo 'Always'
    }

    success {
      echo "Success"
    }
  }
}