pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Cloning repository..."
                git branch: 'main', url: 'https://github.com/Sarra3005/jenkins-test.git'
            }
        }

        stage('Build') {
            steps {
                echo "Running build steps..."
                echo "Date actuelle :"
                bat 'date /t'
                echo "Heure actuelle :"
                bat 'time /t'
            }
        }

        stage('Test') {
            steps {
                echo "Running fake tests..."
                echo "Les tests sont simulés et réussis."
            }
        }

        stage('Archive') {
            steps {
                echo "Archiving pipeline logs..."
                writeFile file: 'result.txt', text: 'Build SUCCESS on Windows'
                archiveArtifacts artifacts: 'result.txt', fingerprint: true
            }
        }
    }
}
