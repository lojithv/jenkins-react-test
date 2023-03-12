pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                /* the return value gets caught and saved into the variable MY_CONTAINER */
                MY_CONTAINER = bat(script: '@docker run -d -i node:18-alpine', returnStdout: true).trim()
                echo "mycontainer_id is ${MY_CONTAINER}"
                /* python --version gets executed inside the Container */
                bat "docker exec ${MY_CONTAINER} node --version "
                /* the Container gets removed */
                bat "docker rm -f ${MY_CONTAINER}"
                }
            }
        }
    }
}