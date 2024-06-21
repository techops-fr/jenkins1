pipeline {
  agent any

  // options {
  //   // failFast pour tous les stages parallel
  //   parallelsAlwaysFailFast()
  // }

  stages {
    stage('Build général en parallèle') {
      failFast: true
      parallel {
        stage('Build Backend') {
          steps {
            echo "Build du backend"
          }
        }
        stage('Build Frontend') {
          steps {
            echo "Build du frontend"
          }
        }
      }
    }
    stage("Déploiement production"){
      steps {
        echo "Deploiement en production"
      }
    }
  }
}