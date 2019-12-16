pipeline {
    agent any
	
    stages {
        stage('clean') {
		agent { label 'docker-slave-agent' } 
            steps {
                sh '''
	
	sudo rm -rf /var/lib/jenkins/workspace/*
			  		
	'''
	
            }
        }
	    
        stage('App') {
		agent { label 'docker-slave-agent' } 
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
