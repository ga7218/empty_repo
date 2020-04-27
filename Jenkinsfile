pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo "Printing $Name"'
          }
        }

        stage('Build2') {
          steps {
            sh 'echo "Hello Build2"'
            sh '''ls -lrth /opt/oracle
cd /opt/oracle/tomcat/github_repo
git clone git@github.com:ga7218/empty_repo.git'''
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
