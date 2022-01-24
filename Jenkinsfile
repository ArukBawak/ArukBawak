pipeline {
  agent any
  stages {
    stage('\'Logging in\'') {
      steps {
        sh 'ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i /home/jenkins/agent/.ssh/jenkins_agent_key jenkins@192.168.157.10 hostname'
      }
    }

  }
}