pipeline {
  agent {
    node {
      label 'master'
    }
  }
  
  tools {
    gradle 'DEFAULT_GRADLE_VERSION'
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
