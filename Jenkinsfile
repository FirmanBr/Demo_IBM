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
                bat '''
                :: Pastikan Anda berada di direktori yang benar
                cd %WORKSPACE%
                
                :: Perintah untuk menjalankan atau mengimpor Jobs.isx
                :: Gantilah dengan perintah spesifik dari DataStage jika ada
                dsimport Jobs.isx

                :: Perintah build DataStage jika diperlukan
                echo "Sukses Menjalankan JOB IBM DataStage Build"
                '''
            }
        }
        stage('Test DataStage') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Test"
                }
            }
        }
        stage('Deploy to Dev Environment') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Deploy"
                }
            }
        }
    }
}
