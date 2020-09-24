pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Buildg...'
      }
    }

    stage('Test') {
      parallel {
        stage('Test Firefox') {
          steps {
            sh 'echo \'Testing Firefox...\''
          }
        }

        stage('Test Chrome') {
          steps {
            sh 'echo \'Testing Chrome...\'; exit 1'
          }
        }

        stage('Test Ddge') {
          steps {
            sh 'echo \'Testing Edge...\''
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployed'
      }
    }

  }
}
