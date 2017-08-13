pipeline {
  agent: none
  stages {
    stage('Build') {
      agent any
      steps {
        checkout scm
        sh 'npm install'
      }
    }
    stage('Test on Linux') {
      agent {
        label 'linux'
      }
      steps {
        sh 'npm test'
      }
    }
    stage('Test on Win') {
      agent {
        label 'linux'
      }
      steps {
        bat 'npm test'
      }
    }
  }
}
