pipeline {
	agent any
	
	stages {
    	stage("Build") {
      		steps {
        		bat 'mvn -B -DskipTests clean package'
				bat 'mvn test'
			}
      	}
    	stage("List all files in directory") {
    		steps {
				bat "dir"
			}
		}
	}
}