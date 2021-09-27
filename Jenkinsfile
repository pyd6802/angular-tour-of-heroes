pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        git(url: 'https://github.com/pyd6802/angular-tour-of-heroes.git', branch: '*/master', poll: true, changelog: true)
      }
    }

    stage('Stage 2') {
      steps {
        powershell 'Hello.ps1'
      }
    }

  }
}