node('master') 
{
    stage('Cont_downl') 
    {
       git 'https://github.com/ravi282/laxsu.git'
    }
    stage('Cont_buil') 
    {
       sh label: '', script: 'mvn package'
    }
    stage('Cont_Deploy')
    {
       sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/Pipe/webapp/target/webapp.war ubuntu@172.31.84.116:/var/lib/tomcat7/webapps/qaenv.war' 
    }
}
