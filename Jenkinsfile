pipeline {
  agent none
  stages {
    stage('init'){
      agent slave1
      steps{
        sh 'sudo apt update'
        sh 'sudo apt install python3-pip'
      }
    
    stage('build') {
      agent slave1
      
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      agent slave1
    
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
