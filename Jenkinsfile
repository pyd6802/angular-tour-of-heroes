pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Step 1'
        echo 'build branch - updated by pyd6802'
        powershell 'write-host "powershell is being called"'
        powershell(returnStatus: true, script: 'npm install')
      }
    }

    stage('deploy') {
      steps {
        echo 'Deploy'
        powershell(returnStatus: true, script: 'npm run ng build')
        echo 'Deploy Complete'
      }
    }

  }
}