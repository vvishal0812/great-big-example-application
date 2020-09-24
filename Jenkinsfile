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

        stage('') {
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
            sh 'npm run cleanup && npm run webpack:build:main'
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