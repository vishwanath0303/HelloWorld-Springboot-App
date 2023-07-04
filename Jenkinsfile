pipeline{
    agent any
    stages{
        stage('Git clone'){
            steps{
                bat "dir"
            }
        }
        
        stage('maven build'){
            steps{
               // sh 'HelloWorld-Springboot-App'
                sh "pwd"
                
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
