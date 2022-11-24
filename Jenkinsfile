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

    stage('deploy') {
      parallel {
        stage('deploy-1') {
          steps {
            build 'deploy-job-1'
          }
        }

        stage('deploy-2') {
          steps {
            build 'deploy-job-2'
          }
        }

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