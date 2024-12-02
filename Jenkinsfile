pipeline {
     agent {
        node {
            label 'saikiran-node'
        }
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['Dev', 'Uat', 'Prod'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment {
        GREETING = "Hello jenkins"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'HOURS')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the code....'
            }
        }
        stage('Deploy') {
           steps {
                echo 'Deploying the code...'
            }
        }
        stage('Params') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }
    post {
        always {
            echo 'I will always say hello'
        }
        success {
            echo 'This will run when pipeline is success'
        }
        failure {
            echo 'This will run when pipeline is failed'
        }
    }
}