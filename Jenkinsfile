node 

{

def mavenhome = tool name: "Maven_3.8.5"

echo "GitHub BranhName ${env.BRANCH_NAME}"
      echo "Jenkins Job Number ${env.BUILD_NUMBER}"
      echo "Jenkins Node Name ${env.NODE_NAME}"
  
      echo "Jenkins Home ${env.JENKINS_HOME}"
      echo "Jenkins URL ${env.JENKINS_URL}"
      echo "JOB Name ${env.JOB_NAME}"   

stage (' checkoutCodeFromSCM ')

{
git credentialsId: 'github_bhanu', url: 'https://github.com/bhanuprasadvantaku/maven-web-application.git'

}

stage('build')

{


sh "${mavenhome}/bin/mvn clean package"

}

/*
stage('ExecuteSonarReport')

{


sh "${mavenhome}/bin/mvn sonar:sonar"

}


stage('upoadingTonexus')

{


sh "${mavenhome}/bin/mvn deploy"

}

stage('DeploytoTomcat')
{

sshagent(['fe7811e0-82f6-458b-80b8-0a017e3a0fe7']) 
{

sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.110.108.174:/opt/apache-tomcat-9.0.62/webapps/"
    
}


}

stage ('mailnotification')

{
emailext body: '''build completed.

regards,
jeevan''', subject: 'maven_web_app-build_status', to: 'djeevan12@gmail.com'

}
*/
}
