pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'building...'
      }
    }

    stage('test') {
      environment {
        stage = 'test'
      }
      parallel {
        stage('test') {
          steps {
            echo 'testing test'
          }
        }

        stage('platform1') {
          steps {
            echo 'testing platform1'
          }
        }

        stage('platform2') {
          steps {
            echo 'testing platform2'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploying...'
      }
    }

  }
}