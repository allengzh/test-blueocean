pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        build 'compile-job-1'
        build 'compile-job-2'
      }
    }

    stage('deploy') {
      steps {
        build 'deploy-job-1'
      }
    }

    stage('sit') {
      steps {
        build 'SIT-test-job'
      }
    }

  }
  environment {
    aa = 'aa'
  }
}