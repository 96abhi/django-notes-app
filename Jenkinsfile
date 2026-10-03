pipeline{
    agent any;
    stages{
        stage("Code"){
            steps{
                git url:"https://github.com/96abhi/django-notes-app.git", branch:"main" 
            }
        }
        stage("Build"){
            steps{
                sh "whoami"
                sh "docker build -t notes-app-elevate-task2 ."
            }
        }
        stage("Test"){
            steps{
                echo "Test Wali Stage"
            }
        }
        stage("Deploy"){
        steps{
            sh "docker-compose up -d"
        }
    }
    }
}
