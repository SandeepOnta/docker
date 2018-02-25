pipeline {
    agent any  
    stages {
        stage('Build Image') {
            steps {
		sh 'docker build -t friendlyhello .'
                sh 'python --version'
            }
	}
	stage('Run Image') {
	    steps {
		sh 'docker run -d -p 4004:80 friendlyhello'
		}
	  }
    }
}
