pipeline {
    agent any

    stages {
        stage('SCM') {
            steps {
                git branch: 'master', url: 'https://github.com/SiriveruJagadeesh/git-flask.git'
            }
        }
       
        stage('Build Docker Image') {
            steps {
                script {
                    
                 sh 'docker build -t jagadeeshsiriveru/server1:v1 .'
                 sh 'docker run -itd -p 1000:4000 jagadeeshsiriveru/server1:v1'  
                }
            }
        }
         
    }
}
