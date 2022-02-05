pipeline {
  agent any
  stages {    
    stage('init'){
      parallel{
      stage('init1'){
      steps{
        sh ' python3 --version'
        
      }
    }
        stage('init2'){
      
      steps{
        sh ' python3 --version '
        
      }
    }
      
    }
    }
    
    stage('build1') {
      
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
      
    
    stage('build2') {
      
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('test2') {
      
    
      steps {
        sh 'python3 test.py'
      }   
    }
  }
}
