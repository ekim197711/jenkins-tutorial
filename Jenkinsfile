pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                    dir("./my-app") {
                    sh 'npm ci'
                }
                 }
            }
        }
        stage('Build') {
            steps {
                
                nodejs(nodeJSInstallationName: 'Node 16.x') {                
                     dir("./my-app") {
                sh 'npm run build'
                }
                 }
            }
        }
        stage('Test') { 
            steps { 
                
                   nodejs(nodeJSInstallationName: 'Node 16.x') {
                    dir("./my-app") {
                    sh 'CI=true npm run test'
                    }
                }
            }
        }
    }
}