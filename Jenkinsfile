pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
          sh 'pip install flake8 pytest pytest-cov'
          sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'pytest ./tests/test_rsvpapp.py'
      }
     
    }
  }
}
