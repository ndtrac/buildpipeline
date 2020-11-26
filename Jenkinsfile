pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:12-alpine'
    }

  }
  stages {
    stage('NPM Install') {
      steps {
        sh 'npm install'
      }
    }

    stage('Newman Install') {
      steps {
        sh 'npm install -g newman'
      }
    }

    stage('') {
      steps {
        sh 'newman run https://www.getpostman.com/collections/631643-f695cab7-6878-eb55-7943-ad88e1ccfd65-JsLv'
      }
    }

  }
}