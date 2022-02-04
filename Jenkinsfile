pipeline {
 agent none
  stages {
    stage('build') {
      agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
    
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
