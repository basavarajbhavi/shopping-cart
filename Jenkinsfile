properties([parameters([choice(choices: 'master\ndev\nrelease', description: '', name: 'branch')]), pipelineTriggers([githubPush()])])
      node{
      
      stage('Scm Checkout') {
          
          
          echo "pulling the changes from the branch ${params.branch}"
          git url: 'https://github.com/basavarajbhavi/shopping-cart.git' , branch:"${params.branch}"
         
           }
            stage('instance') {
                   ec2 cloud: 'devops', template: ''
            }
       }                  
      
