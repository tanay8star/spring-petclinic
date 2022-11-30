pipeline {
  agent any
  stages {
    stage('run ansible') {
      steps {
        sh 'ansible-playbook /vagrant/springboot.yaml'
      }
    }

  }
}