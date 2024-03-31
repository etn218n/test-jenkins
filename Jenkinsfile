pipeline {
    agent any
    
    environment {
        NPM_TOKEN = credentials("NPM_TOKEN")
        NPM_REGISTRY = "duy-npm.com"
        MAIN = "/home/etn218n/storage/projects/publish-upm/main.js"
        STORAGE = "/home/etn218n/storage/verdaccio/storage/"
        JSON = "$WORKSPACE/package.json"
    }
                
    stages {
        stage("Build") {
            steps {
                sh "npm set '//$NPM_REGISTRY/:_authToken=\"$NPM_TOKEN\"'"
                sh "echo '$JSON'"
            }
        }
    }
}
