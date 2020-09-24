pipeline {
  agent {
      docker {
            image 'maven' 
            args '-v /root/.m2:/root/.m2' 
        }
  }
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/vvishal0812/great-big-example-application.git', branch: 'master', poll: true)
      }
    }
      
   stage('Test') {
      steps {
        sh 'mvn -B -DskipTests clean package'
          echo 'Test Skipped'
      }
    }

    stage('End') {
      steps {
        echo 'Completed'
      }
    }

  }
}
