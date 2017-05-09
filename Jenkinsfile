pipeline {
  agent {
    docker {
      image 'golang'
      args 'latest'
    }
    
  }
  stages {
    stage('Install Dependencies') {
      steps {
        sh 'make deps'
      }
    }
    stage('Generate code') {
      steps {
        sh 'make gen'
      }
    }
    stage('Build the binary') {
      steps {
        sh 'make build_static'
      }
    }
  }
}