pipeline {
  agent {
    node {
      label 'master'
    }
  }
  
  tools {
    gradle 'DEFAULT_GRADLE_VERSION'
    jdk 'OPENJDK_DEFAULT_VERSION'
   }
  
  environment {
    JAVA_BINDIR
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
