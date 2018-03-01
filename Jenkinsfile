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
	    stage('Run Docker Stack Deploy') {
		    steps {
			sh 'docker swarm init'
			sh 'docker stack deploy -c docker-compose.yml getstartedlab'
		    }
	    }
    }
}
