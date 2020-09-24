pipeline {
  agent any
  tools {
        maven "Maven"
        nodejs "NodeJS"
   }
  
    stages {
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
        
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

    stage('End') {
      steps {
        echo 'Done'
      }
    }

  }
}
