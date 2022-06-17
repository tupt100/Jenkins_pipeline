pipeline {
    agent any
    stages {
        stage('task1') {
            steps {
                sh 'echo "Hello task1"'
            }
        }
        stage('pullcode') {
            
            steps {
                git 'https://github.com/tupt100/RepolabGIT.git'
                
            }
            
        }
    }
}
