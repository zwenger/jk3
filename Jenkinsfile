pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('mensaje') {
      steps {
        echo 'hola mundo'
      }
    }
    stage('') {
      steps {
        bat(script: 'build/clean.cmd', label: 'clean')
      }
    }
  }
}