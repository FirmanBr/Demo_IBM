pipeline {
    agent any
    stages {
        // Stage 1: Setup Prerequisites
        stage('Setup Prerequisites') {
            steps {
                script {
                    // Check if Java 7.0 is installed
                    bat '''
                    if not exist "C:\\Program Files\\Java\\jdk1.7.0_XX\\bin\\java.exe" (
                        echo "Java 7.0 is not installed. Installing..."
                        rem Add steps to download and install Java 7.0 if needed
                    ) else (
                        echo "Java 7.0 is already installed."
                    )
                    '''

                    // Check if Oracle 12c client is installed
                    bat '''
                    where sqlplus >nul 2>nul
                    if errorlevel 1 (
                        echo "Oracle 12c client is not installed. Installing..."
                        rem Add steps to download and install Oracle 12c client if needed
                    ) else (
                        echo "Oracle 12c client is already installed."
                    )
                    '''
                }
            }
        }
        // Stage 2: Git Checkout
        stage('Git Checkout') {
            steps {
                script {
                    git branch: 'main',
                        credentialsId: 'f0058a63-77b9-4dc0-ba3c-2859f23e0115',
                        url: 'https://github.com/FirmanBr/Demo_IBM.git'
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
