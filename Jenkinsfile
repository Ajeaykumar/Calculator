pipeline{
    agent any
    stages{
        stage('Clone Repository'){
            steps{
                checkout scmGit(branchs: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/Ajeaykumar/Calculator.git' ]])
            }
        }
        stage('Build Docker Image'){
            steps{
                sh 'docker build -t calculator-devops .'
            }
        }
        stage('Run Container'){
            steps{
                sh 'docker run -d -p 5001:5000 calculator-devops'
            }
        }
    }
}