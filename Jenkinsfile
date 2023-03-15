 pipline {
 	agent any
 	stages {
 		stage("install-dep"){
 			steps{
 				sh "sudo yum install docker -y"
 				sh  "sudo yum install git -y"
 				sh "sudo systemctl start docker"
 			}
 		}
 		stage("docker-cmds"){
 			steps{ 				
 				sh "docker run -itdp 80:80 --name pune httpd"
                sh "docker cp index.html pune:/usr/local/apache2/htdocs/"
 			}
 		}
 	}
 }
 
