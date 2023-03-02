pipeline{
  agent{
    label{
      label "dev"
      customWorkspace "/mnt/zz"
    }
  }
  stages{
  stage("tomcat"){
    steps{
      
        sh "chmod -R 777 /mnt/zz"
        sh "sudo yum install git -y"
        sh "sudo yum install docker -y"
        sh "sudo systemctl start docker"
        dir("/mnt/zz/"){
          sh "sudo git clone https://github.com/NishaPatil98/tomcat.git"
          sh "sudo docker build -t tomcat:1.0 . "
          sh "sudo docker run -itdp 8080:8080 tomcat:1.0 "
          
        }
      }
  }
  }
}
