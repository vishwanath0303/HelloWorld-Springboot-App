pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                sh 'git clone https://github.com/vishwanath0303/HelloWorld-Springboot-App.git'
            }
        }
        
        stage('maven build'){
            steps{
                sh 'HelloWorld-Springboot-App'
                
                // sh 'cd ${Workspace}\HelloWorld-Springboot-App'
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
