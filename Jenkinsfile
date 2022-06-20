pipeline {
    agent any
    stages {
        stage('build') {
            steps {
/
                sh 'docker build -t tupt2024/nodejs:v1 .'
          
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
