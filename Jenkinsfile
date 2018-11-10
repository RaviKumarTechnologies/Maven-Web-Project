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
   stage("Deploy App"){
        //for windows running the test cases
        bat 'echo Application deploying.'
        bat 'COPY C:\\Users\\IBM_ADMIN\\.jenkins\\workspace\\Pipeline-job-scriptedway\\target\\*.war C:\\Ravisbackup\\Ravi\\M\\DevOps\\ApacheTomcat\\apache-tomcat-9.0.12\\webapps'
   }
   /*stage("Notification"){
       bat mail bcc: '', body: 'Build done.', cc: 'ravi7164@gmail.com', from: 'ravi_in@yopmail.com', replyTo: '', subject: 'Job created for Pipeline type ', to: 'ravi_ibm1@yopmail.com'
   }*/
	
       
}
