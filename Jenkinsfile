pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o CS193_Karan CS193_Karan.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './CS193_Karan'
                build job: 'PES1UG20CS193-3'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Done'
                
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
