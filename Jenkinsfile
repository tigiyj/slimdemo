pipeline {
  agent {
    node {
      label 'none'
    }

  }
  stages {
    stage('Composer install') {
      agent {
        docker {
          image 'composer:1.10.17'
        }

      }
      steps {
        sh 'docker run --rm --interactive --tty --volume /var/lib/docker/volumes/demojenkins_jenkins_data/_data/workspace/demo_slim_jenkins-pipeline@2:/app composer:1.10.17 install'
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