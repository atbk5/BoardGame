@Library('ci-library-demo@main') _ 
pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {

                git branch: 'main', url: 'https://github.com/atbk5/BoardGame.git'
            }
        }
        stage('Standardized Build') {
            steps {
                script {
                    javaBuild() 
                }
            }
        }
    }
}