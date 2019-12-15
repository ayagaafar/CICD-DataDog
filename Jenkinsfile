pipeline {
    agent { label 'docker-slave-agent' } 
    stages {
        stage('Test') {
            steps {
                sh '''
	
	sudo curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
    	sudo chmod +x /usr/local/bin/docker-compose
	sudo docker ps
    	docker-compose --version
        docker-compose up 
        curl -vk "http://localhost:8123/"
			  		
	'''
            }
        }
    }
}
