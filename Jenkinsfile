pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
      }
    }

    stage('End') {
      steps {
        echo 'Completed'
      }
    }

  }
}