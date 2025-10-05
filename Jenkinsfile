// 1. Declare the Shared Library
// Note: Replace 'demo-library@main' with your actual Library Name and Branch/Tag
@Library('hello-library@hello-lib') _ 

pipeline {
    agent any

    stages {
        stage('Initialization') {
            steps {
                echo "Pipeline execution started in the application repository."
            }
        }
        
        stage('Shared Library Execution') {
            steps {
                script {
                    // 2. Call the global function defined in vars/greetUser.groovy
                    // This single call triggers the entire library flow.
                    greetUser('Student Demo User')
                }
            }
        }
        
        stage('Completion') {
            steps {
                echo "Shared library functions executed successfully!"
            }
        }
    }
}
