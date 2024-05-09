pipeline {
    agent { docker { image 'node:20.11.1-alpine3.19' } }
    stages {
        stage('build') {
            steps {
                sh 'node --version'
            }
        }
        stage('test'){
            steps {
                sh 'node --version'
                sh 'echo hello'
            }
        }
    }
}
