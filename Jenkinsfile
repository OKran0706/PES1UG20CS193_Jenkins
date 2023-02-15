pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o CS193_Karan CS193_Karan.cpp'
                sh 'chmod +x CS193_Karan'
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
                sh 'echo "Hi"'
                
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
