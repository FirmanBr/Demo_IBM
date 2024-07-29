pipeline {
    agent any

    environment {
        DS_PROJECT = 'DataStageProjectName'
        DS_JOB = 'DataStageJobName'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main',
                        credentialsId: 'f0058a63-77b9-4dc0-ba3c-2859f23e0115',
                        url: 'https://github.com/FirmanBr/Demo_IBM.git',
                }
            }
        }
    

        stage('Build') {
            steps {
                script {
                    echo "Building the project..."
                    // Tambahkan perintah build jika ada
                }
            }
        }

        stage('Run DataStage Job') {
            steps {
                script {
                    echo "Running DataStage job..."
                    // Gantilah dengan perintah yang diperlukan untuk menjalankan job di IBM DataStage
                    // Misalnya menggunakan CLI atau API DataStage
   
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Running tests..."
                    // Tambahkan perintah untuk menjalankan test jika ada
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                    // Tambahkan perintah deploy jika ada
                }
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Tambahkan perintah cleanup jika diperlukan
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
  }
}
