pipeline {
    	agent {
    		docker {
        		image 'maven:3-alpine' 
        		args '-v /root/.m2:/root/.m2' 
        	}
    	}
    	stages {
        	stage('Build') { 
            		steps {
				dir ($(WORKSPACE)/maven-hello-world){
					sh 'ls'
                			sh 'mvn -B -DskipTests clean package' 
				}
            		}
        	}
    	}
}
