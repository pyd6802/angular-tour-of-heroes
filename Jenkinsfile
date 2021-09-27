pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Step 1'
        echo 'build branch - updated by pyd6802'
		powershell 'write-host "powershell is being called"'
		powershell 'Set-Location -Path C:\Users\paul\umllsa'
	    powershell '. npm run ng build'
	  }
    }

    stage('deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}