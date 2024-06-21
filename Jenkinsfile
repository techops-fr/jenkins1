pipeline {
  agent any

  triggers {
    cron("*/2 * * * *") // Déclenchement du pipeline toutes les 2 minutes
    poolSCM("*/2 * * * *") // Vérification des modif sur Git toutes les 2 minutes
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
    stage('Deployment production') {
      input {
        message "Voulez-vous déployer en production ?"
        ok "Oui, je déploie en prod"
        submitter 'admin, devops'
        submitParameter 'USER_SUBMIT'
        parameters {
          string(name: "VERSION", defaultValue:"lastest", description:"Une version déployée")
        }
      steps {
        echo "User : ${USER_SUBMIT}"
        echo "Version ${VERSION}"
        echo "Deploy !"
        }
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