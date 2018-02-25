pipeline {
    agent any  
    stages {
        stage('Test') {
            steps {
		sh 'docker build -t friendlyhello .'
                sh 'python --version'
            }
        }
    }
}
