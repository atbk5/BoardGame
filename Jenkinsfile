@Library('jenkins-class-lib@mvn-build') _
pipeline {
    agent any
    
    tools {
        jdk 'jdk17'
        maven 'mvn3'
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'mvn-java-build', url: 'https://github.com/atbk5/BoardGame.git'
            }
        }
        stage('Maven Build') {
            steps {
                script {
                    javaBuild()
                }
            }
        }
    }
}
