pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "hello"'
      }
    }
    stage('Code Quality') {
      steps {
        echo 'hello'
      }
    }
    stage('Security Scanning') {
      steps {
        echo 'Scanning'
      }
    }
    stage('Dev Deploy') {
      steps {
        echo 'Deploy'
      }
    }
    stage('Dev Test') {
      parallel {
        stage('Dev Test') {
          steps {
            echo 'Dev Test'
          }
        }
        stage('Unit Test') {
          steps {
            echo 'Unit Test'
          }
        }
        stage('Performance Test') {
          steps {
            echo 'Perf Test'
          }
        }
      }
    }
    stage('QA Deployment') {
      steps {
        echo 'QA Deploy'
      }
    }
    stage('QA Test') {
      parallel {
        stage('QA Test') {
          steps {
            echo 'QA Test'
          }
        }
        stage('Performance Test') {
          steps {
            echo 'Perf Test'
          }
        }
        stage('Stress Test') {
          steps {
            echo 'Stress Test'
          }
        }
        stage('Integration Test') {
          steps {
            echo 'Integration Test'
          }
        }
      }
    }
    stage('Pre Prod Deployment') {
      steps {
        echo 'PreProd'
      }
    }
    stage('Acceptance Testing') {
      parallel {
        stage('Acceptance Testing') {
          steps {
            echo 'Acceptance Testing'
          }
        }
        stage('DAST Testing') {
          steps {
            echo 'Dynamic Test'
          }
        }
        stage('Security Test') {
          steps {
            echo 'Static Test in prod-like env'
          }
        }
      }
    }
    stage('Deploy to Prod') {
      steps {
        echo 'Prod Deploy'
      }
    }
  }
}