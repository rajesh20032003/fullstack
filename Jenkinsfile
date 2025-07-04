pipeline {
  agent any

  stages {
    stage('Clone') {
      steps {
        git url: 'https://github.com/rajesh20032003/fullstack.git', branch: 'master'
      }
    }

    stage('Build Docker Images') {
      steps {
        script {
          sh 'docker-compose build'
        }
      }
    }

    stage('Run Containers') {
      steps {
        script {
          sh 'docker-compose up -d'
        }
      }
    }
  }
}

