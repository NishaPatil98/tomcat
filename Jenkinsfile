pipeline{
  agent{
    label{
      label "js-0"
    }
  }
  stages{
  stage("tomcat"){
    steps{
      sh "rm -rf /js-0/workspace/zz/"
      
        sh "chmod -R 777 /js-0/workspace/zz/ "
        sh "sudo yum install git -y"
        sh "sudo yum install docker -y"
        sh "sudo systemctl start docker"
       
          sh "sudo git clone https://github.com/NishaPatil98/tomcat.git"
          sh "sudo docker build -t tomcat:1.0 . "
          sh "sudo docker run -itdp 8080:8080 tomcat:1.0 "
          
       
      }
  }
  }
}
