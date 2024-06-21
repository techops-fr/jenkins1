pipeline {
  agent any

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
