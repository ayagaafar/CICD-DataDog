pipeline {
    stages {
		stage ('Test') {
			steps {
				
	                 
	sh "curl -L "https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose"
    sh "chmod +x /usr/local/bin/docker-compose"
    sh "docker-compose --version"
           sh "docker-compose up"
         sh "curl -vk http://localhost:8123/"
				  		

				}
			}
		}
}

