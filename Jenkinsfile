pipeline {
    agent any
    stages {
        stage('Build') {
            environment {
                TestToken = credentials('NPM_TOKEN')
            }
            steps {
                sh "echo '$TestToken'"
            }
        }
    }
}
