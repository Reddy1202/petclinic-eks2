this is java project

we use maven to build application

it connects to the database(mysql)
database info pom.xml
we need to build : mvn clean build -P MySql

we will deloy it in eks k8
code + Docker file


wgere our app will run : tomcat 

what is input : war file

if we need war we have to build




aws ecr get-login-password --region ap-south-1 | sudo docker login --username AWS --password-stdin 897025645367.dkr.ecr.ap-south-1.amazonaws.com


sudo docker build -t 897025645367.dkr.ecr.ap-south-1.amazonaws.com/petclinic-eks:$BUILD_NUMBER .


sudo docker push 897025645367.dkr.ecr.ap-south-1.amazonaws.com/petclinic-eks:$BUILD_NUMBER



pre-req : RDS

1) create the RDS in the EKS VPC
public
private -- create the RDS in the private subnet
2) Allow the RDS-sg  of eks worker node sg
3) allow the jenkins-sg to the rds-sg