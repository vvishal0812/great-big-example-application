pipeline {
  agent any
  stages {
    stage('Pull') {
      parallel {
        stage('Pull') {
          steps {
            git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
          }
        }

        stage('error') {
          steps {
            sh 'npm install rimraf -g'
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Java Test') {
          steps {
            sh 'mvn test'
          }
        }

        stage('Angular Test') {
          steps {
            sh 'npm install'
          }
        }

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