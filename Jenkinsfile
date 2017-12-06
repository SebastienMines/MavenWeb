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
		stage("Deploy on TomCat") {
		steps {
			bat 'tomcat:deploy'
			}
		}
	}
}