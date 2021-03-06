pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'cb511093-ab63-429e-bd87-58e921044dd0', url: 'https://github.com/Monish-Samuel/jenkins_python.git']]])
            }
        }
        
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
    }
}
