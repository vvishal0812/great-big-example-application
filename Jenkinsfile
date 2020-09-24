pipeline {
  agent any
  stages {
    stage('Docker') {
      steps {
        dockerNode(image: 'maven')
      }
    }

    stage('End') {
      steps {
        echo 'Okk'
      }
    }

  }
}