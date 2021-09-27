pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Step 1'
        echo 'build branch - updated by pyd6802'
        sh '. \\Buildstagetoh.ps1'
      }
    }

    stage('deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}