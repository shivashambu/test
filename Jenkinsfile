pipeline {
  agent any
  stages {
    stage('fetch code') {
      steps {
        git(url: 'https://github.com/shivashambu/test.git', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R */var/www/html/'
      }
    }

  }
}