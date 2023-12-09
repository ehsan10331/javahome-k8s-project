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
                	sh "docker build -t ehsan10331/project-app:0.0.1 ."
            		}
        	}
		stage('Push Docker Image') {
           	   steps {
			   withCredentials([usernamePassword(credentialsId: 'hub-creds', passwordVariable: 'hubPwd', usernameVariable: 'hubUser')]) {
  				sh "docker login -u ${hubUser} -p ${hubPwd}
				// sh "docker push ehsan10331/project-app:0.0.1"   
			}
			   sh "docker push ehsan10331/project-app:0.0.1"
		}
	}
	}
}
