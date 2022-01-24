pipeline {
  agent any
  stages {
    stage('\'Logging in\'') {
      steps {
        sh 'ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no -i /home/jenkins/agent/.ssh/jenkins_agent_key jenkins@192.168.157.10 hostname'
        sh '''#!/bin/bash
user=\'aruktest\'
sh  \'useradd -m $user
sh \'passwd $user12\'
sh \'passwd -e $user\'
sh \'chage -m 7 -M 90 $user\'

sh \'if id "$user" >/dev/null 2>&1; then
        echo  "$user created to home dir"
else
        echo  "$user does not exist"
fi\'

sh \'usermod -a -G qadb $user\'
'''
      }
    }

  }
}