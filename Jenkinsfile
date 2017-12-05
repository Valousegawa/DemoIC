pipeline {
	agent any
	
	stages {
    	stage("Build") {
      		steps {
        		bat 'mvn -B -DskipTests clean package'
				bat 'mvn Test'
			}
      	}
    	node {
			def files = findFiles(glob: '*.*') 
			echo """${files[0].name} ${files[0].path} ${files[0].directory} ${files[0].length} ${files[0].lastModified}"""
		}
	}
}