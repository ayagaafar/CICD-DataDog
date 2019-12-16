pipeline {
    agent { label 'docker-slave-agent' } 
	
    stages {
	 
	    
        stage('App') {
		
            steps {
                sh '''

    	docker-compose --version
        docker-compose up -d --force-recreate
	cd ..
	sudo su
	sudo rm -rf ../AscensionDay
	
	'''
	
            }
        }
	 	    
    }
}
