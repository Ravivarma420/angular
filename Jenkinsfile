pipeline {
  agent {
    label 'buildserver'
  }
  stages {
    
    stage ('Checkout')
    {
      steps
      {  
        checkout scm
   
      }
    }
    
    stage ('build')
    {
      steps 
      {
        sh "cd /home/ubuntu/workspace/angular ; sudo apt-get update "
        sh "cd /home/ubuntu/workspace/angular ; sudo curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash - "
        sh "cd /home/ubuntu/workspace/angular ; sudo apt-get install nodejs "
        sh "cd /home/ubuntu/workspace/angular ; sudo npm install -g @angular/cli@11.0.0 -y"
        sh "cd /home/ubuntu/workspace/angular ; sudo ng build "
        sh "sudo ansible-playbook /root/nginx.yml"
       }
       
    }
  }
}
  
    
      
















