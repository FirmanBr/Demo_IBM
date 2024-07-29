pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                script {
                    git branch: 'main',
                        credentialsId: 'f0058a63-77b9-4dc0-ba3c-2859f23e0115',
                        url: 'https://github.com/FirmanBr/Demo_IBM.git'
                }
            }
        }
        stage('Build DataStage') {
            steps {
                script {
                    // Menyusun perintah untuk build DataStage
                    sh '''
                    echo "Sukses Menjalankan JOB IBM DataStage Build"
                    '''
                }
            }
        }
        stage('Test DataStage') {
            steps {
                script {
                    // Menyusun perintah untuk testing DataStage
                    sh '''
                    echo "Sukses Menjalankan JOB IBM DataStage Test"
                    '''
                }
            }
        }
        stage('Deploy to Dev Environment') {
            steps {
                script {
                    // Menyusun perintah untuk deploy DataStage ke environment dev
                    sh '''
                    echo "Sukses Menjalankan JOB IBM DataStage Deploy"
                    '''
                }
            }
        }
    }
}
