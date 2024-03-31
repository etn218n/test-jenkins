pipeline {
    agent any
    
    environment {
        NPM_TOKEN = credentials("NPM_TOKEN")
        NPM_REGISTRY = "duy-npm.com"
        NPM_REGISTRY_URL = "httpS://$NPM_REGISTRY"
        MAIN = "/home/etn218n/storage/projects/publish-upm/main.js"
        STORAGE = "/home/etn218n/storage/verdaccio/storage/"
        JSON = "$WORKSPACE/package.json"
    }
                
    stages {
        stage("Set Registry") {
            steps {
                sh "npm set '//$NPM_REGISTRY/:_authToken=\"$NPM_TOKEN\"'"
            }
        }
        stage ("Publish Package"){
            steps {
                sh "node $MAIN $STORAGE $JSON $NPM_REGISTRY_URL"
            }
        }
    }
}
