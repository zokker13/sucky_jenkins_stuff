#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
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
