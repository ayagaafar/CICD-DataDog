
node {
	agent { label 'docker-slave-agent'}
        stage('App') {
		
            steps {
                sh '''

    	docker-compose --version
        docker-compose up -d --force-recreate
	sudo chown -R jenkins:jenkins app/target 
	
	
	'''
	
            }
        }

}
