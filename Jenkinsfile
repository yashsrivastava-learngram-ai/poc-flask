pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build_test') {
      steps {
        sh 'python3 -m venv venv && . venv/bin/activate && pip install -r requirements.txt && python test.py'
      }
    }
  }
}
