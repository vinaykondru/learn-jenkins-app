pipeline {
    agent any

    stages {
        stage('Node 18 Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    node -v
                    npm -v
                    npm ci
                    npm run build
                '''
            }
        }
    }
}
