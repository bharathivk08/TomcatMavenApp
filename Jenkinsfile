pipeline {
    agent any
    Tools {
       // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN-3.9.8"
    }
    stages {
        stage('Scm') {
            steps {
	    // Get some code from a GitHub repository
                git 'https://github.com/bharathivk08/TomcatMavenApp.git'
                
            }
	 }
	 stage('Build') {
            steps {
	    // To run Maven on a Windows agent, use
  		bat "mvn -Dmaven.test.failure.ignore=true clean package"
	    }	   
         }

    }
}
