pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Build'
        powershell(returnStatus: true, script: 'npm install')
        powershell(returnStatus: true, script: 'npm run ng build')
		echo 'Build Complete'
      }
    }

    stage('deploy') {
      echo 'Deploy'
      try {
        timeout(1) {
         powershell(returnStatus: true, script: 'npm run ng serve')
        }
      }
      catch(err) {echo 'Deploy complete all done - Times Up (1 minute)'
        }
    }   
  }
}  