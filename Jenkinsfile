pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                echo 'dockerfile running'
		docker build -t testing .
	        docker run testing:latest
            }
        }
    }
}
