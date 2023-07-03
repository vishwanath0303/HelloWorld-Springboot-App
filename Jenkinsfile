pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                sh 'git clone https://github.com/shazforiot/HelloWorld-Springboot-App.git'
            }
        }
        
        stage('maven build'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Create Dockerimage'){
            steps{
                sh 'docker build -t vkulkarni0303/springboot:latest .'
            }
        }
        
    }
}
