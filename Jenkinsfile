node {
    stage('Build') {
        echo 'Build Start, Install / Build'
         dir ('toh') {
         powershell(returnStatus: true, script: 'npm install')
         powershell(returnStatus: true, script: 'npm run ng build')}
        } 
    stage('Test') {
       try { 
               dir ('toh') { echo 'Test Phase'
			       powershell(returnStatus: true, script: 'npm install -g newman')
		 		   powershell(returnStatus: true, script: 'newman run ToH.postman_collection.json -n 10' )}
        } catch(err){
          echo 'Test Phase complete'
      }
    }
}