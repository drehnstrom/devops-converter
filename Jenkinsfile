pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    withEnv(["HOME=${env.WORKSPACE}"]) {
        stage('build') {
            steps {
            echo "Install App Requirements"
            sh 'python --version'
            sh 'pip install -r requirements.txt'
          }
        }   
    /* stage('Run') {
      steps {
        echo "Run the Program"
        sh 'python main.py'
      }   
    } */
    }
  }
}