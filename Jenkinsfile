pipeline {
  agent any
  stages {
    stage('Initailize') {
      steps {
        sh 'echo "Initialize"'
      }
    }

//     stage('Checkout') {
//       steps {
//         git 'sample'
//       }
//     }

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
            sh 'sample'
          }
        }

        stage('Resource Server Build') {
          steps {
            sh 'sample'
          }
        }

        stage('Frontend Build') {
          steps {
            sh 'sample'
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
        sh 'sample'
      }
    }

    stage('Deploy to Development') {
      parallel {
        stage('Deploy to DEV') {
          steps {
            sh 'sample'
          }
        }

        stage('Deploy To Stage') {
          steps {
            sh 'sample'
          }
        }

        stage('Deploy To Production') {
          steps {
            sh 'sample'
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