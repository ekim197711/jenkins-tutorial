pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'npm build'
            }
        }
        stage('Test') { 
            steps {
                sh 'CI=true npm test'
            }
        }
    }
}