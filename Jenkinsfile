pipeline {
    agent { label 'docker-slave-agent' } 
	
    stages {
        stage('App') {
            steps {
                sh '''
	sudo rm -rf $WORKSPACE
	sudo docker ps
    	docker-compose --version
        docker-compose up -d --force-recreate
        curl -vk "http://localhost:8123/"
			  		
	'''
		    
            }
        }
	 	    
    }
}
