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
        emailext(subject: '${env.JOB_NAME}', body: 'HE ', attachLog: true, from: 'watchgrafana@gmail.com', to: 'husne.rabbi@emumba.com')
      }
    }
  }
}