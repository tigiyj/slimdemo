pipeline {
  agent {
    docker {
      image 'php:7-alpine'
      args '-p 8080:8080'
    }

  }
  stages {
    stage('Composer install') {
      agent {
        docker {
          image 'composer:latest'
          args '--rm --interactive --tty --volume $PWD:/app    --volume ${COMPOSER_HOME:-$HOME/.composer}:/tmp composer <command>'
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