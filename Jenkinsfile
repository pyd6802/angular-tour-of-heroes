node {
    stage('Initialize') {
        echo 'Clear Directory' {
        powershell(returnStatus: true, script: 'rmdir /S /Q toh')}
        }
    stage('build') {
        echo 'Build Start'
         dir ('toh') {
         powershell(returnStatus: true, script: 'git clone https://github.com/pyd6802/angular-tour-of-heroes')
         powershell(returnStatus: true, script: 'npm install')
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