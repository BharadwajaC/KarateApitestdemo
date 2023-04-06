pipeline {
    agent any
    stages{
        stage('Build Docker image'){
            steps{
                script{
                    sh 'docker --version'
                    sh 'docker build -t maven/base:latest'
                    sh 'docker tag maven/base:apitesting maven/base:latest'
                    sh 'docker push --all-tags'
                }
            }
        }
    }
}