pipeline {
  agent {
    node {
      label 'asd'
    }

  }
  stages {
    stage('mensaje') {
      steps {
        echo 'hola mundo'
      }
    }
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
  }
}