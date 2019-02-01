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
    stage('Email results') {
      steps {
        emailext(subject: 'Done with Jenkins job', attachLog: true, body: 'Here is the job that ran', to: 'kevin@joeporn.nl')
      }
    }
  }
}