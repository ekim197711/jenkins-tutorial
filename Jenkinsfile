pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                sh 'cd ./my-app && npm install'
                }
            }
        }
        stage('Build') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {                
                sh 'cd ./my-app && npm build'
                }
            }
        }
        stage('Test') { 
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                sh 'cd ./my-app && CI=true npm test'
                }
            }
        }
    }
}