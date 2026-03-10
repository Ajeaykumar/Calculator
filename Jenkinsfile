pipeline{
    agent any
    stages{
        stage('Clone Repository'){
            steps{
                git https://github.com/Ajeaykumar/Calculator.git
            }
        }
        stage('Build Docker Image'){
            steps{
                sh 'docker build -t calculator-devops .'
            }
        }
        stage('Run Container'){
            steps{
                sh 'docker run -d -p 5000:5000 calculator-devops'
            }
        }
    }
}