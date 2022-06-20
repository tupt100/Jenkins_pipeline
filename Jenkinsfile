pipeline {
    agent any
    stages {
        stage('task1') {
            steps {
 withDockerRegistry(credentialsId: 'a57694e6-0db0-4834-8478-56e3a1c3e5a3', url: 'https://registry.hub.docker.com/') {
    // some block
}
                sh 'docker build -t nodejs .'
                sh 'docker tag nodejs tupt2024/nodejs'
       
                sh 'docker push tupt2024/nodejs:v1'
                
            }
        }
        
    }
}
