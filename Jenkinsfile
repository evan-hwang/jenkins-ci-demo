pipeline {
  agent any
  stages {
    stage('Initailize') {
      steps {
        sh 'echo "Initialize"'
      }
    }

    stage('Checkout') {
      steps {
        git(url: 'https://github.com/evan-hwang/jenkins-ci-demo.git', branch: 'master')
      }
    }

    stage('Unit Test') {
      steps {
        echo 'Unit Test'
      }
    }

    stage('Browser Test') {
      steps {
        echo 'Browser Test'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh './gradlew build'
          }
        }

        stage('Auth Server Build') {
          steps {
            echo 'sample'
          }
        }

        stage('Resource Server Build') {
          steps {
            echo 'sample'
          }
        }

        stage('Frontend Build') {
          steps {
            echo 'sample'
          }
        }

      }
    }

    stage('Publish Reports') {
      steps {
        echo 'sample'
      }
    }

    stage('Docker Tag & Push') {
      steps {
        echo 'sample'
      }
    }

    stage('Deploy to Development') {
      parallel {
        stage('Deploy to DEV') {
          steps {
            sh 'echo "Deploy Success"'
          }
        }

        stage('Deploy To Stage') {
          steps {
            echo 'sample'
          }
        }

        stage('Deploy To Production') {
          steps {
            echo 'sample'
          }
        }

      }
    }

    stage('End') {
      steps {
        echo 'sample'
      }
    }

  }
}