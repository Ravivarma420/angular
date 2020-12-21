pipeline{
  agent{
    label''
  }
  stages{
    
    stage('Checkout')
    {
      steps
      {  
      sh "checkout scm"
   
      }
    }
    
    stage('build')
    {
      steps 
      {
        sh "cd /home/ubuntu/workspace//Angular-jembo ; npm install "
      }
    }
    stage('build2')
    {
      steps
      {
      sh "cd /home/ubuntu/workspace//            ; ng build "
      }
    }
    
    
    stage('Deploying into nginx')
    {
      steps
      {
        node('ansible')
        {
          sh "sudo ansible-playbook /root/nginx.yml"
        }
      } 
    }
  }
}
  
    
      















}
