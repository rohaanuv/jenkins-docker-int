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
 				sh "docker run -itdp 80:80 --name mumbai httpd"
                sh "docker cp index.html mumbai:/usr/local/apache2/htdocs/"
 			}
 		}
 	}
 }
 
