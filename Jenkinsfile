pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "building"'
                build 'PES1UG21CS088-1'
                sh 'g++ main2.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "testing"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "deploying"' 
                sh 'echo "deployed"'
            }
        }
    }
    post{
        failure{
            error 'pipeline failed'
        }
    }
}
