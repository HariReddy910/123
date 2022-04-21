pipeline{
     agent any
    stages{
         stage('Checkout-SCM')
		 {
		     steps{
			            checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
				        doGenerateSubmoduleConfigurations: false, 
				        extensions: [], 
				        submoduleCfg: [],
				        userRemoteConfigs: [[credentialsId: '2a239424-0e74-41e9-8034-488a00f90311',
			            url: 'https://github.com/HariReddy910/123.git']]])
			        }
		   }
	     stage('Build-stage')
		 {
		    steps{
		               sh label: '', script: 'mvn package'
		             }
	     }
	    
	/*    stage("Deployment-AppServer"){
            steps{
              echo "hi"
             sh label: '', script: 'scp /var/lib/jenkins/workspace/MVN-Project/target/app.war ubuntu@172.31.2.23:/opt/tomcat9/webapps/123.war'
           }
        
        }*/
    
    
    }
}
