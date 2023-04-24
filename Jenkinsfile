pipeline{
    agent any
    stages{
        stage('git checkout'){
        steps{
            git credentialsId: 'githubcred', url: 'https://github.com/pradeep281998/composetest.git'
        }
    }
        stage('docker build'){
        steps{
            sh 'docker  build -t pradeep/compose:v1 .'
        }    
    }
        stage('doceker-compose'){
        steps{
            sh 'docker compose up -d'
        }
        }
        
}
}
