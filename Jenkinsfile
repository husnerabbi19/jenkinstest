pipeline {
  agent {
    docker {
      image 'alpine'
    }

  }
  stages {
    stage('TEST') {
      steps {
        sh 'echo "Hello"'
        emailext(subject: '$DEFAULT_SUBJECT', body: '$DEFAULT_CONTENT', from: 'watchgrafana@gmail.com', to: '[[$class: \'DevelopersRecipientProvider\']')
      }
    }
  }
}