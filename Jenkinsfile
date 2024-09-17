pipeline {
    agent any
    
    stages{
        stage('code'){
            steps {
                git url: 'https://github.com/yogeshyadava/node-todo-labapp-cicd.git', branch: 'main'
            }
        }
        stage('Build and Test'){
            steps {
                sh 'sudo docker --version'
                sh 'sudo docker pull learnitguide/busapp'
                sh 'sudo docker images'
            }
        }
        stage('Deploy the build'){
            steps {
                sh 'sudo docker run -d -it --name MYAPP2 -p 99:8001 learnitguide/busapp'
            }
        }
    }
}    
