pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Build'
        powershell(returnStatus: true, script: 'npm install')
		echo 'Build Complete'
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