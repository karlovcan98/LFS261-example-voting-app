stage('Trigger deployment') {
     agent any
     environment{
       def GIT_COMMIT = "${env.GIT_COMMIT}"
     }
     steps{
       echo "${GIT_COMMIT}"
       echo "triggering deployment"
       // passing variables to job deployment run by vote-deploy repository Jenkinsfile
       build job: 'deployment', parameters: [string(name: 'DOCKERTAG', value: GIT_COMMIT)]
     }    
  }
