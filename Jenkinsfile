pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
    }
    
    post {
        always {
            echo 'Build and test completed'
        }
        success {
            echo 'Build succeeded! Tests passed.'
        }
        failure {
            echo 'Build failed! Tests may have failed.'
        }
    }
}
