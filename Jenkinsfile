pipeline {
    agent any
    stages {
        environment {
            NPM_TOKEN = credentials('NPM_TOKEN')
            NPM_REGISTRY = 'duy-npm.com'
        }
        stage('Build') {
            steps {
                sh "echo '//$NPM_REGISTRY/:_authToken="$NPM_TOKEN'"
            }
        }
    }
}
