pipeline {
  agent {
    docker {
      image 'node:14-alpine'
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

    stage('Run Postman') {
      steps {
        sh 'newman run https://www.getpostman.com/collections/631643-f695cab7-6878-eb55-7943-ad88e1ccfd65-JsLv'
      }
    }

  }
}