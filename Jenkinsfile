pipeline {
    agent any
    stages {
        // Stage 1: Git Checkout
        stage('Git Checkout') {
            steps {
                script {
                    git branch: 'main',
                        credentialsId: 'f0058a63-77b9-4dc0-ba3c-2859f23e0115',
                        url: 'https://github.com/FirmanBr/Demo_IBM.git'
                }
            }
        }
        stage('Setup Prerequisites') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Proses Test"
                }
            }
        }
        
        // Stage 3: Build DataStage
        stage('Build DataStage') {
            steps {
                echo "Sukses Menjalankan JOB IBM DataStage Proses BUILD"
            }
        }
        // Stage 4: Test DataStage
        stage('Test DataStage') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Proses Test"
                }
            }
        }
        // Stage 5: Deploy to Dev Environment
        stage('Deploy to Dev Environment') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Proses Deploy"
                }
            }
        }
    }
}
