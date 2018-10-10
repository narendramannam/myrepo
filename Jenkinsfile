pipeline {
  agent {
    node {
      label 'master'
    }
  }
  
  stages {
    
    stage('checkout') {
      steps {
        checkout scm 
      }
    }
    stage('build') {
      steps {
        sh '''
          java -version
          gradle -version
        '''
      }
    }
  }
}
