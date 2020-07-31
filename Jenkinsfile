pipeline {
      
  agent any
  stages {
        
    stage('Git') {
      steps {
             properties([parameters([choice(choices: ['master', 'dev', 'release'], description: 'branching and merging strategy', name: 'branches')]), pipelineTriggers([githubPush()])])
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/basavarajbhavi/shopping-cart.git']]])
        
             }
     }
     
  
    
 
    
            
    
  }
}
