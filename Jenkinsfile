// 1. Declare the Shared Library
// Note: Replace 'demo-library@main' with your actual Library Name and Branch/Tag
@Library('hello-library@hello-lib') _ 
import com.demo.UtilityClass

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
                    greetUser('Student Demo User')

                    def u = new UtilityClass(this)
                    u.runSampleMethod('Student Demo User 2')
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
