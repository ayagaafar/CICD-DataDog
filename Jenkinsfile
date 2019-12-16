agent {
node {
	label 'docker-slave-agent'
	
        stage('App') {
		
           
                sh '''

    	docker-compose --version
        docker-compose up -d --force-recreate
	sudo chown -R jenkins:jenkins app/target 
	
	
	'''
	
            }
        

}
}
