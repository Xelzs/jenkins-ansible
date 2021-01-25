properties([pipelineTriggers([githubPush()])])

pipeline {
    agent { dockerfile true }
    
    stages {
      stage('Launch playbook') {
        steps {
          sh 'ansible-playbook -i inventory.ini playbook.yml'
        }
      }
    }
}
