pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('Testing stage') {
      steps {
        sh 'mvn clean'
        sh 'mvn --projects biojava-alignment test'
      }
    }

  }
}