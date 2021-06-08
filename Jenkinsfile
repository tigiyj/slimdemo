pipeline {
  agent any
  stages {
    stage('Composer install') {
      agent {
        docker {
          image 'composer:latest'
          args 'docker run --rm --interactive --tty --volume $PWD:/app composer install'
        }

      }
      steps {
        echo 'composer install'
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