pipeline{
    agent any 
    stages{
        stage('DockerBuildPush'){
            steps{
                sh "docker pull nginx"
                echo "******printing the images********"
                sh 'docker images'
                sh 'docker tag nginx shiva261/nginxdevops:b7'
                sh 'docker push shiva261/nginxdevops:b7'
            }
        }
    }
}
