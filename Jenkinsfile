pipeline {
  agent {
    node {
      label "js-0"
      customWorkspace "/home/pipeline"
  
    }
  }
  stages{
  stage("tomcat"){
    steps{
      
      sh "rm -rf /home/pipeline/*"
      sh "chmod -R 777 /home"
    
       sh "git clone https://github.com/NishaPatil98/tomcat.git"
      
      
          
       
      }
  }
  }
}
