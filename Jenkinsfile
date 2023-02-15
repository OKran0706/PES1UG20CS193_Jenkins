pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh script: 'g++ -o CS193_Karan CS193_Karan.cpp', shell: '/bin/bash'
                sh script: 'chmod +x CS193_Karan', shell: '/bin/bash'
            }
        }
        stage('Test') {
            steps {
                sh './CS193_Karan'
                build job: 'PES1UG20CS193-1'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
                sh script: 'cat hi.txt', shell: shell: '/bin/dash'
                
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline completed.'
        }
            
        failure {
            echo 'Pipeline failed.'
        }
    }
}
