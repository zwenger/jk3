pipeline {
agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
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
