pipeline {
    agent any

    // Comment
    /* Block comment */
    // add # Before Command to prevent Execution 

    stages {
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
                   npm install
                   npm run build
                   ls -la
                '''
            }
        }
    }
}