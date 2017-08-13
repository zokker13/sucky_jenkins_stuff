#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
    stage('Build') {
      agent any
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
        sh 'echo hola'
      }
    }
  }
}
