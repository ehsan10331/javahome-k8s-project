pipeline {
    agent any
	stages {
        	stage('Build Artifact') {
           	   steps {
                	sh "mvn clean package"
            		}
        	}
		stage('Build Docker Image') {
           	   steps {
                	sh "docker build -t ehsan10331/Java-app:0.0.1 ."
            		}
        	}
	}
}
