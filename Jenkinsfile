pipeline{
  agent{
    label{
      label "js-0"
      customWorkspace "/mnt/zz"
    }
  }
  stages{
  stage("tomcat"){
    steps{
      sh "sudo rm -rf /mnt/zz/*"
      sh "sudo chmod 777 /mnt"
      sh "sudo docker system prune -a -f"
        sh "sudo yum install docker -y"
        sh "sudo systemctl start docker"
      dir("/mnt/zz"){
        sh "sudo git init"
        
   
       
          sh "sudo git clone https://github.com/NishaPatil98/tomcat.git"
          sh "sudo docker build -t tomcat:1.0 . "
          sh "sudo docker run -itdp 8080:8080 tomcat:1.0 "
          sh "sudo exec -itd tomcat:1.0 bash "
      }
          
       
      }
  }
  }
}
