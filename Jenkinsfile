pipeline {
  agent {
    node {
      label 'mycloud-swarm'
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