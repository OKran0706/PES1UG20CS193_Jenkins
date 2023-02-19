pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o CS193_Karan CS193_Karan.cpp'
                build job: 'PES1UG20CS193-1'
            }
        }
        stage('Test') {
            steps {
                sh './CS193_Karan'
                
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
//                 sh 'cat hi.txt'
                
            }
        }
    }
    
    post {    
        failure {
            echo 'Pipeline failed.'
        }
    }
}
