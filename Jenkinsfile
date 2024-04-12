pipeline {
  agent {
    node {
      label 'ubn'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''ls
pwd
date'''
      }
    }

    stage('test1') {
      parallel {
        stage('test1') {
          steps {
            echo 'test1 successful'
          }
        }

        stage('test par') {
          steps {
            echo 'test par succ'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh '''df -h
'''
        echo 'deploy sucessful'
      }
    }

    stage('Prod') {
      steps {
        echo 'End Deployment ready to gp for production'
      }
    }

  }
  environment {
    name = 'jbn'
  }
}