pipeline {
    agent {
        node {
            label 'saikiran-node'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building....'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..........'
            }
        }
    }
    post {
        success {
            echo 'This pipeline is successfully done'
        }
        failure {
            echo 'This pipeline is failed'
        }
    }
}