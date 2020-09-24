pipeline {
  agent any
  stages {
    stage('SCM Pull') {
      steps {
        git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
      }
    }

    stage('Test') {
      steps {
        nodejs('NodeJs') {
          sh 'node install'
          tool 'Maven'
          sh 'mvn clean compile install'
        }

      }
    }

    stage('End') {
      steps {
        echo 'End'
      }
    }

  }
}