pipeline {
    agent any
    stages {
        stage('Install') {
            steps {
                 dir("./my-app") {
                nodejs(nodeJSInstallationName: 'Node 16.x') {
                sh 'npm install'
                }
                 }
            }
        }
        stage('Build') {
            steps {
                
                nodejs(nodeJSInstallationName: 'Node 16.x') {                
                     dir("./my-app") {
                sh 'npm build'
                }
                 }
            }
        }
        stage('Test') { 
            steps { 
                dir("./my-app") {
                   nodejs(nodeJSInstallationName: 'Node 16.x') {
                    sh 'CI=true npm test'
                    }
                }
            }
        }
    }
}