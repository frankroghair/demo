pipeline {
  agent any
  stages {
    stage('commit') {
      parallel {
        stage('inc debug') {
          steps {
            echo 'inc debg'
          }
        }
        stage('inc_release') {
          steps {
            echo 'inc release'
          }
        }
        stage('release') {
          steps {
            echo 'release'
          }
        }
      }
    }
    stage('acceptance') {
      parallel {
        stage('acceptance test') {
          steps {
            echo 'acceptance test'
          }
        }
        stage('acceptance smoke') {
          steps {
            echo 'acceptance smoke'
          }
        }
      }
    }
    stage('regression') {
      parallel {
        stage('performance') {
          steps {
            echo 'performance'
          }
        }
        stage('unit') {
          steps {
            echo 'unit'
          }
        }
        stage('component') {
          steps {
            echo 'component'
          }
        }
      }
    }
    stage('Report') {
      parallel {
        stage('excel') {
          steps {
            echo 'excel'
          }
        }
        stage('mail') {
          steps {
            echo 'mail'
          }
        }
      }
    }
    stage('Finished') {
      steps {
        echo 'The end'
      }
    }
  }
}