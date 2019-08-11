pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'python3 -m pytest'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging....'
                sh 'docker build -t gcr.io/doug-rehnstrom/jenkins-converter:v0.2 .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}