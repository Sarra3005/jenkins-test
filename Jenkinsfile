pipeline {
    agent any

    stages {

        stage('Git') {
            steps {
                echo "🔵 Phase 1 : Récupération du code source"
                git branch: 'main', url: 'https://github.com/Sarra3005/jenkins-test.git'
            }
        }

        stage('Compilation') {
            steps {
                echo "🟡 Phase 2 : Compilation"
                bat '''
                echo ===== Compilation en cours =====
                echo Simulation d'une compilation...
                echo OK
                '''
            }
        }

        stage('Tests') {
            steps {
                echo "🟢 Phase 3 : Tests"
                bat '''
                echo ===== Exécution des tests =====
                echo Tous les tests simulés sont PASS
                '''
            }
        }
    }

    post {
        success {
            echo "🎉 Pipeline terminé avec succès"
        }
        failure {
            echo "❌ Pipeline en erreur"
        }
    }
}
