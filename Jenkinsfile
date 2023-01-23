pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
      steps {
          sh 'sudo pip install -r requirements.txt --user'
      }
    }
    stage('test') {
      steps {
        sh 'sudo pytest ./tests/test_rsvpapp.py'
      }
     
    }
  }
}
