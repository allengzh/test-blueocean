pipeline {
  agent any
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            echo 'hello'
          }
        }

        stage('world') {
          steps {
            echo 'world'
            echo 'end'
          }
        }

      }
    }

    stage('apple') {
      steps {
        echo 'apple'
        sh 'echo $aa'
      }
    }

  }
  environment {
    aa = 'aa'
  }
}