pipeline {
  agent {
    node {
      label 'master'
    }
  }
  
  tools {
    gradle 'defaultgradle'
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
