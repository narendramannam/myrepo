pipeline {
  agent {
    node {
      label 'master'
    }
  }
  
  tools {
    gradle 'DEFAULT_GRADLE_VERSION'
    jdk 'JDK_DEFAULT_VERSION'
   }
  
  environment {
    JAVA_BINDIR="${tool 'JDK_DEFAULT_VERSION'}/bin"
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
