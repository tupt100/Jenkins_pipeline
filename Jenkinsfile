pipeline {
    agent any
    stages {
        stage('build') {
            steps {
// withDockerRegistry(credentialsId: 'a57694e6-0db0-4834-8478-56e3a1c3e5a3', url: 'https://login.docker.com/') {
    // some block
//}
                
             //   withDockerRegistry(credentialsId: 'docker-hub', url: 'https://registry.hub.docker.com/') {
    // some block
//}
                sh 'docker build -t tupt2024/nodejs:v1 .'
             //   sh 'docker tag nodejs tupt2024/nodejs'
       
              //  sh 'docker push tupt2024/nodejs:v1'
                
            }
        }
        stage('Login') {

			steps {
				sh 'docker login -u tupt2024 -p Admin@2022'
			}
		}
        
        stage('Push') {

			steps {
                sh 'docker push tupt2024/nodejs:v1'
			}
		}
        
    }
}
