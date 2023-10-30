pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'eae29205-3246-4932-b4bf-6b3600beb14b', url: 'https://github.com/sahubabu/printfile.git']]) 
            }
        }
        stage('build'){
            steps {
             git branch: 'main', credentialsId: 'eae29205-3246-4932-b4bf-6b3600beb14b', url: 'https://github.com/sahubabu/printfile.git'
             sh 'python3 hello.py'
            }
        }
        stage('deployment'){
            steps {
                echo "DONE"
            }
        }
    }
}
