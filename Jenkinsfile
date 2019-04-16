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
        emailext(subject: '$DEFAULT_SUBJECT', body: '"${env.BUILD_URL} has result ${currentBuild.result}"', from: 'watchgrafana@gmail.com', to: 'husne.rabbi@emumba.com')
      }
    }
  }
}