pipeline {
    agent any 
    options { timestamps () }
    tools {nodejs "nodejs"}

    stages {
        stage('Prep frontend') {
            steps {
                dir('ussd_fe') {
                    sh 'npm install'
                    sh 'npm run build'
                }          
            }
        }
        stage('Deploy') {
            steps {
                sh '/usr/local/bin/docker-compose down -v'
                sh '/usr/local/bin/docker-compose up -d --build'
            }
        }
    }
}