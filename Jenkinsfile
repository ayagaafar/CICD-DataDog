pipeline {
    agent { label 'docker-slave-agent' } 
	
    stages {
	 
        stage('clean') {
		
            steps {
                sh '''
	sudo rm -rf jenkins:jenkins /var/lib/jenkins/workspace/*
	
			  		
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
