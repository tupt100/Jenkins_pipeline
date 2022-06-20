pipeline {
    agent { label'Slave' }
	
	environment {
        REGISTRY_NAME               = credentials('REGISTRY_NAME')
        DOCKER_REGISTRY_USERNAME    = credentials('DOCKER_REGISTRY_USERNAME')
        DOCKER_REGISTRY_PASSWORD    = credentials('DOCKER_REGISTRY_PASSWORD')
    }
	
	
	
    stages {
        stage('build') {
            steps {

                sh 'docker build -t tupt2024/nodejs:v1 .'
          
            }
        }
        stage('Login') {

			steps {
				sh 'docker login -u ${DOCKER_REGISTRY_USERNAME} -p ${DOCKER_REGISTRY_PASSWORD}'
			}
		}
        
        stage('Push') {

	 steps {
                sh 'docker push tupt2024/nodejs:v1'
			}
		}
        
    }
}
