pipeline {
    agent any
    stages {
        stage('Build') {
            environment {
                Token = credentials('NPM_TOKEN')
            }
            steps {
                echo '$Token'
            }
        }
    }
}
