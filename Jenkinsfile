node {
    stage('build') {
        echo 'Build Start, Clone / Install / Run'
         dir ('toh') {
         powershell(returnStatus: true, script: 'git clone https://github.com/pyd6802/angular-tour-of-heroes')
         powershell(returnStatus: true, script: 'npm install')
         powershell(returnStatus: true, script: 'npm run ng build')}
        } 
    stage('deploy') {
       try { 
           timeout(2) {
               dir ('toh') { echo 'Deploy Start, process will run for 2 minutes'
           powershell(returnStatus: true, script: 'npm run ng serve') }
           }
        } catch(err){
          echo 'Deploy completed after timeout (2 minutes)'
      }
    }
}