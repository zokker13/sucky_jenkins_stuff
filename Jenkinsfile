pipeline {
  agent: none
  stages {
    state('Build') {
      agent any
      steps {
        checkout scm
        sh 'npm install'
      }
    }
    state('Test on Linux') {
      agent {
        label 'linux'
      }
      steps {
        sh 'npm test'
      }
    }
    state('Test on Win') {
      agent {
        label 'linux'
      }
      steps {
        bat 'npm test'
      }
    }
  }
}
