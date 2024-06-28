pipeline {
    agent any
    
    stages{
        stage("Code Clone"){
            steps{
                git url: "https://github.com/swastik7777/DevOps_pratice.git", branch: "master"
            }
        }
        stage("Code Test"){
            steps{
                echo "Code Test Sucessfully"
            }
        }
        stage("Code Build"){
            steps{
                sh "docker build . -t flask:v1"
            }
        }
        stage("Code Deploy"){
            steps{
                sh "docker run -d -p 5000:5000 flask:v1"
            }
        }
        
    }
}
