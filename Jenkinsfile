pipeline {
    agent any
	
    stages {
	 agent { label 'docker-slave-agent' }   
        stage('clean') {
		
            steps {
                sh '''
	sudo chown -R jenkins:jenkins /var/lib/jenkins/workspace/*
	
			  		
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
