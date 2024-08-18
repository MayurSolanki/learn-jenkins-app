pipeline {
    agent any

    // Comment
    /* Block comment */
    // add # Before Command to prevent Execution 

    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs() // Cleans up the workspace
            }
        }

        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                   ls -la
                   node --version
                   npm --version
                   npm ci
                   npm run build
                   ls -la
                '''
            }
        }
    }
}