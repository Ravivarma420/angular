pipeline{
  agent{
    label 'buildserver'
  }
  stages{
    
    stage('Checkout')
    {
      steps
      {  
        checkout scm
   
      }
    }
    
    stage('build')
    {
      steps 
      {
        sh "cd /home/ubuntu/workspace/angular/Angular-JumpSart ; sudo npm install "
      }
    }
    stage('build2')
    {
      steps
      {
      sh "cd /home/ubuntu/workspace/angular/Angular-JumpStart ; ng build "
      }
    }
    stage('Deploying into nginx server')
    {
      steps
      {
          sh "sudo ansible-playbook /root/nginx.yml"
       }
       
    }
  }
}
  
    
      















}
