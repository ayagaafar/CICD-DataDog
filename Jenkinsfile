pipeline {
    agent { label 'docker-slave-agent' } 
	
    stages {
	 
        stage('clean') {
		
            steps {
                sh '''
	sudo unlink /var/lib/jenkins/workspace/AscensionDay@tmp
	sudo unlink /var/lib/jenkins/workspace/AscensionDay
	sudo rm -rf /var/lib/jenkins/workspace/AscensionDay@tmp
	sudo rm -rf /var/lib/jenkins/workspace/AscensionDay
			  		
	'''
	
            }
        }
	    
        stage('App') {
		
            steps {
                sh '''
	
	sudo docker ps
    	docker-compose --version
        docker-compose up -d --force-recreate
        curl -vk "http://localhost:8123/"
			  		
	'''
	
            }
        }
	 	    
    }
}
