node{

def mavenHome = tool name: 'maven3.8.5'

echo "The Job name is: ${env.JOB_NAME}"
echo "The Build number is: ${env.BUILD_Number}"
echo "The node name is: ${env.NODE_NAME}"

//Checkout Code State
stage('CheckoutCode'){
git branch: 'development', credentialsId: '7674aa9e-1ef2-4eda-9f62-7ccbdcf061d0', url: 'https://github.com/thivagark-apps/maven-web-application.git'

} 

//Build
stage('Build'){
sh "${mavenHome}/bin/mvn clean package"
}
 
  /*
//Execute SonarQube Report
stage('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

//UploadArtifacts Into Nexus
stage('UploadArtifactsIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}

//Deploy App into Tomcat Server
stage('DeployApp'){
sshagent(['5aaeb706-fdc2-4b49-9c6f-f5b0adca21c7']) {
   sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.38.85:/opt/apache-tomcat-9.0.68/webapps/"
}
}

*/

}//node closing
