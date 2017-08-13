#!/usr/bin/env groovy

pipeline {
  agent any

  stages {
    stage('Build linux') {
      agent 'linux'
      steps {
        sh 'echo hola'
      }
    }
  }
}
