pipeline {
    agent any
    parameters { // Les paramatres avec "Build with parameters" dans l'interface
      booleanParam(name: "DEPLOY_PROD", defaultValue: false, description: "Déploiement en Production")
    }
    stages {
        stage('Build Stage') {
            steps {
                echo 'Bonjour le monde - Etape de Build'
            }
        }
        stage('Déployer en production') {
            when {
                allOf { // Toutes les conditions doivent être rempli
                    branch 'main' // La branch est main
                    environment name: 'DEPLOY_PROD', value: true // DEPLOY_PROD est vrai
                }
            }
            steps {
                echo 'Déploiement en cours'
            }
        }
    }
}
