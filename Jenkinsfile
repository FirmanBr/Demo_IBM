pipeline {
    agent any
    environment {
        JAVA_HOME = ''
        ORACLE_HOME = ''
    }
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
     stage('Setup Prerequisites') {
            steps {
                script {
                    // Check and install Java 7.0 if not already installed
                    sh '''
                    if ! java -version 2>&1 | grep -q "java version \"1.7\""; then
                        echo "Java 7.0 is not installed. Installing..."
                        sudo apt-get update
                        sudo apt-get install -y openjdk-7-jdk
                    else
                        echo "Java 7.0 is already installed."
                    fi
                    '''

                    // Check and install Oracle 12c 64-bit client if not already installed
                    sh '''
                    if ! command -v sqlplus &> /dev/null; then
                        echo "Oracle 12c client is not installed. Installing..."
                        # Assuming the Oracle 12c client zip file is available in the Jenkins workspace
                        sudo apt-get update
                        sudo apt-get install -y alien libaio1
                        cd $WORKSPACE
                        unzip oracle-instantclient12.2-basic-12.2.0.1.0-1.x86_64.zip
                        cd instantclient_12_2
                        sudo alien -i *.rpm
                        sudo ldconfig
                    else
                        echo "Oracle 12c client is already installed."
                    fi
                    '''
                }
            }
        }        
        stage('Build DataStage') {
            steps {
                echo "Sukses Menjalankan JOB IBM DataStage Proses BUILD"
            }
        }
        stage('Test DataStage') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Proses Test"
                }
            }
        }
        stage('Deploy to Dev Environment') {
            steps {
                script {
                    echo "Sukses Menjalankan JOB IBM DataStage Proses Deploy"
                }
            }
        }
    }
}
