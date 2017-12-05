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
				bat "for /f \"delims=\" \%a in ('cd') do @for /f \%b in ('dir /b /a') do @echo \%a\\\%b"
			}
		}
	}
}