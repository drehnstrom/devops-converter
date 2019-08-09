pipeline {
  agent { docker { image 'python:3.7.2' } }
  withEnv(["HOME=${env.WORKSPACE}"]) {
  stages {
    
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