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
        emailext(subject: '"STARTED: Job \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\'"', body: '"""<p>STARTED: Job \'${env.JOB_NAME} [${env.BUILD_NUMBER}]\':</p>         <p>Check console output at "<a href="${env.BUILD_URL}">${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>"</p>"""', attachLog: true, from: 'watchgrafana@gmail.com', to: 'husne.rabbi@emumba.com')
      }
    }
  }
}