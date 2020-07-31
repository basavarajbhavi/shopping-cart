pipeline {
       properties([parameters([choice(choices: ['master', 'dev', 'release'], description: 'branching and merging strategy', name: 'branches')]), pipelineTriggers([githubPush()])])
  agent any
  stages {
        
    stage('Git') {
      steps {
           checkout([$class: 'GitSCM', branches: [[name: '*/']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/basavarajbhavi/shopping-cart.git']]]
        
             }
     }
     
  
    
 
    
            
    
  }
}
