pipeline {
    agent any
    
    tools {
        jdk 'jdk17'
        maven 'mvn3'
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/atbk5/BoardGame.git'
            }
        }
        stage('Compile') {
            steps {
                sh "mvn compile"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Build') {
            steps {
                sh "mvn package"
            }
        }
    }
}
