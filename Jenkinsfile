pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'py -m pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        sh 'py test.py'
      }
      post {
        always {
          junit 'test-reports/*.xml'
        }
      }    
    }
  }
}
