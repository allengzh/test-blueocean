pipeline {
  agent any
  stages {
    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            build 'compile-job-1'
            build 'compile-job-2'
          }
        }

        stage('') {
          steps {
            sonarScanner(gitRepoUrl: 'asd', branch: 'asd', scannerDir: 'ad', exclusions: 'ad')
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