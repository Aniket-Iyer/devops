pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Java Program...'
                sh 'javac prog.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java Program...'
                sh 'java prog'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
                sh 'mkdir -p deployment'
                sh 'cp prog.class deployment/'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}