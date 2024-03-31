pipeline {
    agent any
    stages {
        stage('Build') {
            environment {
                NPM_TOKEN = credentials('NPM_TOKEN')
                NPM_REGISTRY = 'duy-npm.com'
            }
            steps {
                sh "echo '//$NPM_REGISTRY/:_authToken=$NPM_TOKEN'"
            }
        }
    }
}
