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
  
    stage('tag and push docker image'){

steps{

sh(script:'docker login -u sumeshkanayi -p Sia123')
sh(script:'docker tag sumeshkanayi/devops-maven sumeshkanayi/devops-maven:1.0.2')
sh(script:'docker push sumeshkanayi/devops-maven:1.0.2')

}





}
  
      stage('Run and test container '){

steps{


sh(script:'docker run -it --name devops-test sumeshkanayi/devops-maven:1.0.2')
sh(script:'docker exec -it devops-test ls /')

}





}







}








}
