pipeline{

agent 'any'

stages{

stage('build maven'){

steps{

sh(script:'mvn clean install')

}





}

  
  stage('build docker image'){

steps{

sh(script:'docker build --tag sumeshkanayi/devops-maven .')

}





}






}








}
