node {
    stage('build') {
        echo 'Build Start, Install / Build'
         dir ('toh') {
         powershell(returnStatus: true, script: 'npm install')
         powershell(returnStatus: true, script: 'npm run ng build')}
        } 
    stage('Test') {
       try { 
               dir ('toh') { echo 'Deploy Start, process will run for 2 minutes'
			       powershell(returnStatus: true, script: 'npm install -g newman')
		 		   powershell(returnStatus: true, script: 'newman run ToH.postman_collection.json')}
        } catch(err){
          echo 'Deploy completed after timeout (2 minutes)'
      }
    }
}