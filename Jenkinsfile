 pipline {
 	agent {
 		lable "built"
 	}
 	stages {
 		stage("install-dep"){
 			steps{
 			sh "sudo yum install docker -y"
 				sh  "sudo yum install git -y"
 				sh "sudo systemctl start docker"
 			}
 		}
 		
 		}
 	}
 }
