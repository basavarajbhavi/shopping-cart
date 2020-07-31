pipeline {
      properties([parameters([choice(choices: ['master', 'dev', 'release'], description: 'branching and merging strategy', name: 'branching')])])
      
      node{
                   
  stages {
        
            stage('Scm checkout'){
                  echo "pulling changes from the branching ${params.branching}"
                  git url:'https://github.com/basavarajbhavi/shopping-cart.git', branching:"${params.branching}"
            }
            
  }
}
