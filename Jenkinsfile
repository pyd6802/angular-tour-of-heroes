pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'Build from Github'
      }
    }

    stage('Stage 2') {
      steps {
        powershell 'Hello.ps1'
      }
    }

  }
}