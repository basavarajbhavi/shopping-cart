pipeline {
      properties([parameters([choice(choices: 'master\ndev\nrelease', description: '', name: 'branch')]), pipelineTriggers([githubPush()])])
      
 agent any 
stages {       
      stage('Git') {
      steps {
            echo "pulling the changes from the branch ${params.branch}"
            git url: 'https://github.com/basavarajbhavi/shopping-cart.git' , branch:"${params.branch}"
   
           
           }
                   }
       }                  
      }
