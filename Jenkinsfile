pipeline {
	agent any
	
	stages {
    	stage("Build") {
      		steps {
        		bat 'mvn package'
			}
      	}
		stage("Test") {
		steps {
			bat 'mvn test'
			}
		}
		stage("Quality control Sonar") {
		steps{
			bat 'mvn sonar:sonar'
			}
		}
		stage("TomCat Deploiement") {
		steps {
			bat 'mvn tomcat:deploy'
			}
		}
	}
}