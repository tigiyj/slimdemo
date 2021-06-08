pipeline {
  agent any
  stages {
    stage('Composer install') {
      agent any
      steps {
        sh 'docker run --rm --interactive --volume /var/lib/docker/volumes/demojenkins_jenkins_data/_data/workspace/demo_slim_jenkins-pipeline@2:/app composer:1.10.17 install'
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