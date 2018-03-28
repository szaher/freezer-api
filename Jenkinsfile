pipeline {
  agent any
  stages {
    stage('checkout') {
      parallel {
        stage('checkout') {
          steps {
            sh 'whoami'
          }
        }
        stage('') {
          steps {
            sh 'ls -lh'
          }
        }
      }
    }
    stage('check-python') {
      parallel {
        stage('check-python') {
          steps {
            sh 'which python'
          }
        }
        stage('') {
          steps {
            sh 'pwd'
          }
        }
      }
    }
    stage('build') {
      steps {
        echo 'Building ...'
      }
    }
    stage('Notify') {
      steps {
        echo "nothing here"
      }
    }
  }
}
