pipeline {
    agent {
    	docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2 -u root:root' 
        }
    }
    stages {
        stage('Build') { 
            steps {
		sh 'ls'
		dir ('/maven-hello-world/') {
		    sh 'ls'
                    sh 'mvn -B -DskipTests clean package'
		}
            }
        }
    }
}
