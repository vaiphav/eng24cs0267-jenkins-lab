pipeline {
    agent any
    environment {
        STUDENT = 'Vaibhav (ENG24CS0267)'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Source code checked out by SCM'
                sh 'ls -la'
            }
        }
        stage('Test') {
            steps {
                echo 'Running pytest unit tests...'
                sh 'python3 -m pytest -v'
            }
        }
        stage('Report') {
            steps {
                echo "Lab report generation for ${env.STUDENT}"
                sh 'date > pipeline-timestamp.txt'
            }
        }
    }
    post {
        always {
            echo 'Jenkinsfile pipeline run completed'
        }
    }
}
