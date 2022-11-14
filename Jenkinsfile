pipeline {
  agent any
  stages {
    stage('mvn build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('sonar') {
      steps {
        sh '''mvn sonar:sonar \\
  -Dsonar.projectKey=devopsandfriends \\
  -Dsonar.host.url=http://localhost:9000 \\
  -Dsonar.login=5d1d414f2255fa13304a02bd96ac61e7f0492ea1'''
      }
    }

    stage('run') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('') {
      steps {
        sh 'cp target/petclinic.jar ./vagrant/'
      }
    }

  }
}