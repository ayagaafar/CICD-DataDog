pipeline {
    agent { label 'docker-slave-agent' } 
    stages {
        stage('Test') {
            steps {
                sh '''
	
	curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    	chmod +x /usr/local/bin/docker-compose
    	docker-compose --version
        docker-compose up --build
        curl -vk "http://localhost:8123/"
			  		
	'''
            }
        }
    }
}
