pipeline {
    agent any
    
    environment {
        NPM_TOKEN = credentials('NPM_TOKEN')
        NPM_REGISTRY = 'duy-npm.com'
    }
                
    stages {
        stage('Build') {
            steps {
                sh "npm set '//$NPM_REGISTRY/:_authToken=\"$NPM_TOKEN\"'"
            }
        }
    }
}
