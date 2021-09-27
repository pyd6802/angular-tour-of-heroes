pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Step 1'
        echo 'build branch - updated by pyd6802'
		powershell 'dir'
	    powershell '. \npm run ng build'
	  }
    }

    stage('deploy') {
      steps {
        echo 'Deploy'
      }
    }

  }
}