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
                    // Contoh: Menjalankan skrip shell yang memanggil perintah DataStage
                echo"Menjalankan Proses BUILD"
                }
            }
        }
    }
}
