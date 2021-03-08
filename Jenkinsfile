pipeline {
	agent any
	    stages {
	        stage('Clone Repository') {
	        /* Cloning the repository to our workspace */
	        steps {
	        checkout scm
	        }
	   }
	   stage('Build Image') {
	        steps {
	        sh 'docker build . -f Dockerfile -t churnmodel'
	        }
	   }
	   stage('Run Image') {
	        steps {
	        sh 'docker run -d -p 4000:8000 --name churn churnmodel'
	        }
	   }
	   stage('Testing'){
	        steps {
	            echo 'Testing..'
	            }
	   }
    }
}
