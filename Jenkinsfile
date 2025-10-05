@Library('ci-library-demo@main') _ 
pipeline {
    agent any

    tools {
        jdk 'jdk17'
        maven 'mvn3'
    }

    stages {
        stage('Checkout') {
            steps {

                git branch: 'main', url: 'https://github.com/atbk5/BoardGame.git'
            }
        }
        stage('Standardized Build') {
            steps {
                script {
                    javaBuild('mvn3') 
                }
            }
        }
    }
}