#!groovy

node {
	   
	/*stage('Checkout'){

          checkout scm
       }

       stage('BuildArtifact'){

         // sh 'mvn install'
	       
	       sh 'mvn clean'
       }
	   
      stage('Sonar') {
                    //add stage sonar
                   // sh 'mvn sonar:sonar'
                } */
				
				
	node {
	   stage("CheckoutSourceCode"){
			git credentialsId: 'bc98c91a-5669-4f42-8529-9847248a2d91', url: 'https://github.com/RaviKumarTechnologies/Maven-Web-Project.git'
	   }
	   stage("Test"){
			//for windows running the test cases
			bat 'mvn test'
	   }
	   stage("build"){
			//for windows running the test cases
			bat 'mvn clean deploy'
	   }
	   stage("SonarQube Report"){
			//for windows running the test cases
			bat 'mvn sonar:sonar'
	   }
	   /*stage("Deploy App"){
			//for windows running the test cases
			bat 'echo Application deploying.'
			bat 'COPY $WORKSPACE/target/*.war C:/Ravisbackup/Ravi/M/Apache Tomcat/apache-tomcat-9.0.12/webapps'
	   }*/
	   /*stage("Notification"){
		   bat 'emailext attachLog: true, body: '', compressLog: true, recipientProviders: [developers()], replyTo: 'ravi7164@gmail.com', subject: 'Build Status', to: 'ravi7164@gmail.com''
	   }*/
	   }
	}
	
       
}
