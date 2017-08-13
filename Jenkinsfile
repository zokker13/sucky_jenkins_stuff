#!/usr/bin/env groovy

pipeline {
  agent none

  stages {
    stage('Build Win') {
      agent {
        label 'win'
      }
      steps {
        checkout scm
        bat 'npm install'
        bat 'npm test'
      }
    }
    stage('Build linux') {
      agent {
        label 'linux'
      }
      steps {
        checkout scm
        sh 'npm install'
        sh 'npm test'
      }
    }
  }
}
