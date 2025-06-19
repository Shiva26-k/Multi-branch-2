pipeline{
    agent any 
    environment{
        DOCKER_CREDS = credentials('dockerhub_creds')
    }
    stages{
        stage('DockerBuildPush'){
            steps{
                sh "docker pull nginx"
                echo "******printing the images********"
                sh "docker images"
                sh "docker tag nginx nginxdevops:b7"
                sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                sh "docker push shiva261/docker/nginxdevops:b7"
            }
        }
    }
}
