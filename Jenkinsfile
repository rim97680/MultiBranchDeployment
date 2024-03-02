pipeline{
 agent any
  stages{
    stage('clone the code'){
     steps{
     git branch: 'nodejs', url: 'https://github.com/rim97680/MultiBranchDeployment.git'  
      }
     }
     stage('build the image '){
     steps{
       sh 'docker build -t myimg .'
      }
     }
    stage('run the image'){
     steps{
       sh 'docker run -d -P myimg'
       sh 'docker ps -a '
      }
     }
    
  }
    
}
