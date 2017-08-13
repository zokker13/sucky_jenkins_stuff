#!/usr/bin/env groovy

pipeline {
  agent none

  stages {
    stage('Build Win') {
      agent {
        label 'win'
      }
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'gityo', url: 'https://github.com/zokker13/sucky_jenkins_stuff']]])
        bat 'npm test'
      }
    }
    stage('Build linux') {
      agent {
        label 'linux'
      }
      steps {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'gityo', url: 'https://github.com/zokker13/sucky_jenkins_stuff']]])
        sh 'npm test'
      }
    }
  }
}
