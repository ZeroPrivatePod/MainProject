pipeline {
  agent {
    node {
      label 'MacPro'
    }

  }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'hello world'
          }
        }

        stage('analyses') {
          steps {
            echo 'nanlyse'
          }
        }

      }
    }

    stage('devloy') {
      parallel {
        stage('devloy') {
          steps {
            retry(count: 4) {
              sleep 5
            }

          }
        }

        stage('upload_products') {
          steps {
            echo 'products'
          }
        }

      }
    }

  }
}