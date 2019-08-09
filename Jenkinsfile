pipeline {
  agent { docker { image 'python:3.7.2' } }
  
  stages {
    stage('Run the Unit Tests') {
        steps {
            withEnv(["HOME=${env.WORKSPACE}"]) {
                echo "Install App Requirements"
                sh 'python --version'
                sh 'pip install -r requirements.txt'
                sh 'python main_test.py'
                }
        }   
    }
    stage('Build the Docker Container') {
      steps {
        echo "Building the Docker Container"
        sh 'ls -a'
        sh 'docker --version'
      }   
    }
    }
}