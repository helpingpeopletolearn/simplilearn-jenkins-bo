pipeline {
  agent any
  stages {
    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Fetch code') {
      steps {
        git(url: 'git@github.com:helpingpeopletolearn/simplilearn-jenkins-bo.git', branch: 'main')
      }
    }

    stage('Deploy App') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}