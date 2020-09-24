pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
      }
    }

    stage('Angular Test') {
      steps {
        sh 'npm install'
      }
    }

    stage('End') {
      steps {
        echo 'Done'
      }
    }

  }
  tools {
    maven 'Maven'
    nodejs 'NodeJS'
  }
}