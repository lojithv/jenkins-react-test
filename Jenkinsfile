pipeline {
    agent { docker { image 'node:18-alpine' } }
    stages {
        stage('build') {
            steps {
                sh 'npm start'
            }
        }
    }
}