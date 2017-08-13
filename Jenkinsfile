#!/usr/bin/env groovy

node {
  stage('checkout') {
    checkout scm
  }
  stage('Test on linux') {
    agent {
      label 'linux'
    }
    sh 'npm install'
    sh 'npm test'
  }
  stage('Test on Windows') {
    agent {
      label 'win'
    }
    bat 'npm install'
    bat 'npm test'
  }
}
