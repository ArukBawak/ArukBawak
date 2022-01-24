pipeline {
  agent any
  stages {
    stage('\'Logging in\'') {
      steps {
        sh '''ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i /home/jenkins/agent/.ssh/jenkins_agent_key jenkins@192.168.157.10 hostname

'''
      }
    }

    stage('add user') {
      steps {
        sh '''sh  \'useradd -m aruktest
sh \'passwd aruktest\'
sh \'passwd -e aruktest\'
sh \'chage -m 7 -M 90 aruktest\'
sh \'usermod -a -G qadb aruktest\''''
      }
    }

  }
}