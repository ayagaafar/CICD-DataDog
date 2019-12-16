pipeline {
    agent { label 'docker-slave-agent' } 
	
    stages {
        stage('App') {
            steps {
                sh '''
	
	sudo docker ps
    	docker-compose --version
        docker-compose up -d --force-recreate
        curl -vk "http://localhost:8123/"
	sudo rm -rf /var/lib/jenkins/workspace/AscensionDay		  		
	'''
		    
            }
        }
	 	    
    }
}
