pipeline {
  agent any
  stages {
    stage('\'Logging in\'') {
      steps {
        sh '''ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i /home/jenkins/agent/.ssh/jenkins_agent_key jenkins@192.168.157.10 hostname

'''
      }
    }

    stage('create user ') {
      steps {
        sh '''ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i /home/jenkins/agent/.ssh/jenkins_agent_key jenkins@192.168.157.10 hostname
useradd -m aruktest
passwd aruktest123
passwd -e aruktest
chage -m 7 -M 90 aruktest
usermod -a -G qadb aruktest
getent passwd aruktest
getent group qadb'''
      }
    }

  }
}