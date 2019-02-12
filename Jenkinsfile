pipeline {
  agent any
  stages {
    stage('Echo something') {
      parallel {
        stage('Echo something') {
          steps {
            echo 'something'
            sleep 10
          }
        }
        stage('Echo something else') {
          steps {
            echo 'something else'
            sleep 10
          }
        }
      }
    }
    stage('Ask for email') {
      steps {
        input 'Send results to email?'
      }
    }
    stage('Email') {
      steps {
        emailext(subject: 'Results', body: 'HYG', attachLog: true)
      }
    }
    stage('Echo latest') {
      steps {
        echo 'Special for Niels'
      }
    }
  }
}