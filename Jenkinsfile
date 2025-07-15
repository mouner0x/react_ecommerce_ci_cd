pipeline{

  agent any
  stages{
    stage("build")
    docker build -t mouner0x/webapp:v${build_number} .
stage("deploy"){
  docker login -u $user -p $pass
  docker push mouner0x/webapp:v${build_number}
  kubectl apply -f deployment.yml
    kubectl apply -f svc.yml

}
  
}
