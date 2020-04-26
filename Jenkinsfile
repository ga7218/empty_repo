pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "$Name"'
          }
        }

        stage('Build2') {
          steps {
            sh 'echo "Hello Build2"'
          }
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo "Hello world"'
      }
    }

  }
  environment {
    Name = 'Fred Flintstone'
  }
}