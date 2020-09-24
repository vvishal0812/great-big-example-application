pipeline {
  agent any
  stages {
    stage('Tools') {
      steps {
        tool 'Maven'
      }
    }

    stage('Pull') {
      steps {
        git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('End') {
      steps {
        echo 'Done'
      }
    }

  }
}