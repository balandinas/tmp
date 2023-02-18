pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/balandinas/tmp1.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'building'
        cat 'main.txt'
      }
    }

    stage('deploy1') {
      parallel {
        stage('deploy1') {
          steps {
            sleep 3
            echo 'deploy msg 1'
          }
        }

        stage('deploy2') {
          steps {
            sleep 7
            echo 'deploy2'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'testing'
      }
    }

  }
}
