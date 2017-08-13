#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
    stage('Build') {
      agent {
        label 'linux'
      }
      steps {
        checkout scm
        sh 'npm install'
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
