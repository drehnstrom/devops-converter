pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
        echo "Install App Requirements"
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        echo "Run the Unit tests"
        sh 'pytest'
      }   
    }
  }
}