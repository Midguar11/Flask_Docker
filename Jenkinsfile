pipeline {
    agent any
    stages{
        stage('Git Clone'){
            agent any
            steps{
                git branch: 'master', url: 'https://github.com/Midguar11/Flask_Docker.git'
            }
        }
        
       stage('Docker Run'){
            agent any       
            steps{
                sh 'sudo docker container prune'
                sh 'sudo docker-compose up -d'
                sh 'sudo docker compose ps'
            }
        }
    
    }
}