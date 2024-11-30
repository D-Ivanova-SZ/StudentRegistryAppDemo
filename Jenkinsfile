pipeline {
    agent any

    stages {
        stage("Checkout") {
            steps {
                git branch: 'main', url: 'https://github.com/D-Ivanova-SZ/StudentRegistryAppDemo'
            }
        }

        stage("Install dependencies") {
            steps {
                script {
                    bat 'npm install'
                }
            }
        }

        stage("Start application") {
            steps {
                script {
                    bat 'start /b npm start'
                }
            }
        }

        stage("Run tests") {
            steps {
                script {
                    bat 'start npm test'
                }
            }
        }
    }

    post {
        always {
            echo "CI pipeline completed"
        }
    }
}