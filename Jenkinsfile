pipeline {
    agent {
        docker {
            image 'node:lts-buster-slim'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm start'
            }
        }
        // stage('Deliver') { 
        //     steps {
        //         sh 'chmod +x ./jenkins/scripts/deliver.sh' 
        //         input message: 'Finished using the web site? (Click "Proceed" to continue)' 
        //         sh 'chmod +x ./jenkins/scripts/kill.sh' 
        //     }
        // }
    }
}
