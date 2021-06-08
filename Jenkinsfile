pipeline {
  agent any
  stages {
    stage('Composer install') {
      agent {
        docker {
          image 'composer:latest'
        }

      }
      steps {
        sh 'docker run --rm --interactive --tty --volume $PWD:/app composer install'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }

  }
}