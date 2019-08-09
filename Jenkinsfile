pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
        echo "Install App Requirements"
        withEnv(["HOME=${env.WORKSPACE}"]) {
                    sh 'pip install --user -r requirements.txt'
                }
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