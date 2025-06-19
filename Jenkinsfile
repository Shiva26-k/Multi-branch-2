pipeline{
    agent any 
    stages{
        stage('DockerBuildPush'){
            steps{
                sh "docker pull nginx"
                echo "******printing the images********"
                sh 'docker images'
            }
        }
    }
}
