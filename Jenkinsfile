pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                sh 'npm build'
                }
            }
        }
        stage('Test') { 
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                sh 'CI=true npm test'
                }
            }
        }
    }
}