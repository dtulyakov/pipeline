pipeline {
  agent any
  stages {
    stage('pwd') {
      parallel {
        stage('1') {
          steps {
            sh 'pwd'
          }
        }
        stage('ls') {
          steps {
            sh 'ls'
          }
        }
        stage('uname') {
          steps {
            sh 'uname'
          }
        }
      }
    }
    stage('sleep') {
      parallel {
        stage('sleep') {
          steps {
            sleep 10
          }
        }
        stage('sleep 20') {
          steps {
            sleep 20
          }
        }
      }
    }
    stage('end') {
      agent any
      environment {
        NAME = 'MF'
      }
      steps {
        sh 'echo ${NAME}'
      }
    }
  }
}