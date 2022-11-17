pipeline {
    agent any
    tools {
        nodejs '16.14.0'
    }
    stages {
        stage('TEST') {
            steps {
                sh 'npm version'
                sh 'npm install'
            }
        }
    }
}
