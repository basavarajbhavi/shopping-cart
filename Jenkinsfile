pipeline {
      properties([parameters([choice(choices: ['master', 'dev', 'release'], description: 'branching and merging strategy', name: 'branching')])])
      
      node{
            stage('Scm checkout'){
                  echo "pulling changes from the branching ${params.branching}"
                  git url:'https://github.com/basavarajbhavi/shopping-cart.git', branching:"${params.branching}"
            }
      }
 agent any{  
stages {       
      stage('Git') {
      steps {
   
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/basavarajbhavi/shopping-cart.git']]])
        
             }
     }


  }
}      
}
