pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('python_env') {
      steps {
        sh 'python3 -m venv env'
      }
    }
    stage('activate_env') {
      steps {
        sh 'source env/bin/activate'
      }
    }
    stage('build') {
      steps {
        sh 'pip3 install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}
