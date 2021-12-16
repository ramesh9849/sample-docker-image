pipeline{
  agent any
  environment{
    DOCKER_CONFIGID = credentials('jenkins-training-docker-config-json')
  }  
  stage{
    stage("hello"){
      sh "docker build -t jenkinstraining.azurecr.in/sample-docker-image-65635:$BUILD_TAG,"
    }
  }
  stage("Path docker image to container registry'){
        steps{
          sh "export DOCKER_CONFIG=${dirname $DOCKER_CONFIG): docker push jenkinstraining.azurecr.io/sample-docker-image-65635:$BUILD_NUMBER"
        }
        }
        }
        }
