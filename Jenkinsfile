pipeline {
  agent none
  stages {
    stage('init'){
      agent {
        label 'slave1'
      }
      steps{
        sh 'sudo apt update'
        
      }
    }
    
    stage('build') {
      agent {
        label 'slave1'
      }
      
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      agent {
        label 'slave2'
      }
    
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
