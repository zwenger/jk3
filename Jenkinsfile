pipeline {
  agent any
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
    stage('notification') {
      steps {
        slackSend(botUser: true, channel: 'alfred', color: 'green', message: 'asd', baseUrl: 'https://app.slack.com/client/TJRL6EF2B/CJS0R89JA', attachments: 'asdasd', teamDomain: 'alfred-espacio', username: 'jenkins', token: 'nzUct8WUftCkmvjT3wCgcljd')
      }
    }
  }
}