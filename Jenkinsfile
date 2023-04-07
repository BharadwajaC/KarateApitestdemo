pipeline {
    agent any
    stages{
        stage('Build Docker image'){
            steps{
                script{
                    sh 'docker --version'
                    sh 'docker build -build-arg CACHEBUST=$(date +%s) -t maven/base .'
                    sh 'docker run -d -i -t maven/base /bin/sh'
                }
            }
        }
    }
}