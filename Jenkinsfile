pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        echo 'Hello World, have another one - trebles all round'
      }
    }

    stage('Stage 2') {
      steps {
        powershell '. "$ENV:$WORKSPACE\\Hello.ps1"'
      }
    }

  }
}