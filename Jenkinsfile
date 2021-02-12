pipeline {
  agent any
  stages {
    stage('Buzz Build ') {
      steps {
        sh './jenkins/build.sh'
        archiveArtifacts(artifacts: 'test.zip', fingerprint: true)
      }
    }

    stage('Buzz Test') {
      steps {
        sh './jenkins/test-all.sh'
      }
    }

  }
}