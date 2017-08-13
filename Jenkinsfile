#!/usr/bin/env groovy

pipeline {
  agent none

  stages {
    stage('Build') {
      agent {
        label 'win'
      }
      steps {
        checkout scm
        bat 'npm install'
      }
    }
    stage('Build linux') {
      agent {
        label 'linux'
      }
      steps {
        sh 'npm test'
      }
    }
    stage('Build Win') {
      agent {
        label 'win'
      }
      steps {
        bat 'npm test'
      }
    }
  }
}
