pipeline {
      
  agent any
  stages {
        
    stage('Git') {
      steps {
            
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/basavarajbhavi/shopping-cart.git']]])
        
             }
     }
     
  
    
 
    
            
    
  }
}
