pipeline {
    agent any

    environment {
        DS_PROJECT = 'DataStageProjectName'
        DS_JOB = 'DataStageJobName'
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/FirmanBr/Demo_IBM.git', branch: 'main'
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
                    //sh '''
                    //dsjob -run -wait $DS_PROJECT $DS_JOB
                    '''
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
