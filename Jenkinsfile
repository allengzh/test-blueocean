pipeline {
  agent any
  stages {
    stage('compile') {
      parallel {
        stage('compile-1') {
          steps {
            build 'compile-job-1'
          }
        }

        stage('compile-2') {
          steps {
            build 'compile-job-2'
          }
        }

      }
    }

    stage('deploy-1') {
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