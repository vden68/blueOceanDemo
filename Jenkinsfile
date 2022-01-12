pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/vden68/blueOceanDemo.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deployto Dev_1') {
          steps {
            sleep 30
            echo 'finished'
          }
        }

        stage('Deploy to Dev_2') {
          steps {
            sleep 50
            echo 'completed'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing'
      }
    }

  }
}