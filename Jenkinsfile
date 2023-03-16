 pipeline  {
 	agent {
		label "s1"
	}
 	stages {
 		stage("install-dep"){
 			steps{
 				sh "sudo yum install docker -y"
 				sh  "sudo yum install git -y"
 				sh "sudo systemctl start docker"
				sh "sudo rm -rf *"
 			}
 		}
		stage("mumbai-container"){
 			steps{
				sh "sudo git clone -b mumbai https://github.com/rohaanuv/jenkins-docker-int.git mumbai" 				
 				sh "sudo docker run -itdp 8083:80 --name mumbai httpd"
                sh "sudo docker cp /mnt/s1/workspace/test/mumbai/index.html mumbai:/usr/local/apache2/htdocs/"
 			}
 		}
		stage("pune-container"){
 			steps{
				sh "sudo git clone -b pune https://github.com/rohaanuv/jenkins-docker-int.git pune" 				
 				sh "sudo docker run -itdp 8082:80 --name pune httpd"
                sh "sudo docker cp /mnt/s1/workspace/test/pune/index.html pune:/usr/local/apache2/htdocs/"
 			}
 		}
		stage("nagpur-container"){
 			steps{
				sh "sudo git clone -b nagpur https://github.com/rohaanuv/jenkins-docker-int.git nagpur" 				
 				sh "sudo docker run -itdp 8081:80 --name nagpur httpd"
                sh "sudo docker cp /mnt/s1/workspace/test/nagpur/index.html nagpur:/usr/local/apache2/htdocs/"
 			}
 		}
 		
 	}
 }
 
