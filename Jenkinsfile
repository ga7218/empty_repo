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
        sh '/opt/oracle/tomcat/apache-maven-3.6.3/bin/mvn -v'
      }
    }

  }
  environment {
    Name = 'Fred Flintstone'
  }
}