node {
    stage('build') {
        echo 'Build Start T1'
         dir ('toh')
        {powershell(returnStatus: true, script: 'npm install')
        powershell(returnStatus: true, script: 'npm run ng build')}
        } 
    stage('deploy') {
       try { 
           timeout(1) {
               dir ('toh') { echo 'Deploy will run for 1 minute'
           powershell(returnStatus: true, script: 'npm run ng serve') }
           }
        } catch(err){
          echo 'Deploy complete all done - Times Up (1 minute)'
      }
    }
}
