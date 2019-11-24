pipeline {
agent any
        tools { 
        maven 'Maven 3.3.9' 
        jdk 'jdk8' 
    }
  stages {
    stage('clean') {
      steps {
        sh './clean.sh'
      }
    }
    stage('setup') {
      steps {
        sh './setup.sh'
      }
    }
    stage('build') {
      steps {
        sh './build_x64.sh'
      }
    }
    stage('test') {
      steps {
        sh './test.sh'
      }
    }
    stage('notification') {
      steps {
        slackSend(message: 'el circuito de integracion finalizo con exito')
      }
    }
  }
}
