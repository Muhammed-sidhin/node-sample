pipeline {
    agent any
    tools {
        nodejs '16.14.0'
    }
    stages {
        stage('TEST') {
            steps {
                script {
                    echo "Testing Application"
                }
            }
        }
        stage ('Build') {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "Building Application"
                    sh 'npm version'
                    sh 'npm install'
                }
            }
        }
        stage ('Deploy') {
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                script {
                    echo "Deploy Application"
                }
            }
        }
    }
}
