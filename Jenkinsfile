pipeline {
    agent any
	tools {
		maven 'mvn'
	}

    stages {
        stage('Build Artifact') {
            steps {
                sh 'mvn clean package'
            }
        }
		
		// stage('stage2') {
  //           steps {
  //               echo 'Hello World'
  //           }
  //       }
		
		// stage('stage3') {
  //           steps {
  //               echo 'Hello World'
  //           }
        }
    }
