pipeline {
    agent any
    stages {
        stage('task1') {
            steps {
  withDockerRegistry(credentialsId: 'b3ecb878-3f0b-4c45-a3a6-b434c255a2fa', url: 'https://hub.docker.com') {
    // some block
}
                sh 'docker build -t nodejs .'
                sh 'docker push  nodejs '
                
            }
        }
        
    }
}
