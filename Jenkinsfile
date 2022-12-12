pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/arshavardan/html-repo.git', branch: 'main', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy application ') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}