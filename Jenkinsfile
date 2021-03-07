pipeline {
    agent any

    stages {        
        stage('Build'){
            steps{
                git credentialsId: 'cb511093-ab63-429e-bd87-58e921044dd0', url: 'https://github.com/Monish-Samuel/jenkins_python.git'
                bat 'python jenkpyth.py'
            }
        }
        stage('Test'){
            steps{
                echo 'the job has been tested'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deployed successfully'
            }
        }
    }
}
