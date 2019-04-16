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
        mail(subject: 'TEST', body: 'TEST234', from: 'watchgrafana@gmail.com', to: 'husne.rabbi@emumba.com')
      }
    }
  }
}