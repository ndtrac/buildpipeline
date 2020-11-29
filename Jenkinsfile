pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'npm install'
      }
    }

    stage('Install Newman') {
      steps {
        bat 'npm install -g newman'
      }
    }

    stage('Run Postman') {
      steps {
        bat 'newman run https://www.getpostman.com/collections/631643-f695cab7-6878-eb55-7943-ad88e1ccfd65-JsLv'
      }
    }

  }
}