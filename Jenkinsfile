properties([gitLabConnection(gitLabConnection: '', jobCredentialId: ''), parameters([string(defaultValue: 'aws-eu', name: 'DISK_NAME'), string(defaultValue: 'machine', name: 'MACHINE_NAME'), string(defaultValue: '1000', name: 'TARGET_GB')])])
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/EduardUsatchev/gitproject.git'
            }
        }
    stages {
        stage('Run Python') {
            steps {
                sh 'python main.py'
            }
        }
    }
}