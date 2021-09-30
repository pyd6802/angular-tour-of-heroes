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
      try {
        timeout(1) {
		echo 'Deploy'
        powershell(returnStatus: true, script: 'npm run ng serve')
        }
      }
    } catch(err) {	
	   echo 'Deploy complete all done - Times Up (1 minute)'
    }
  }
}