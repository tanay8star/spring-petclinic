pipeline {
  agent any
  stages {
    stage('run ansible') {
      steps {
        sh '''echo "vagrant" | ansible-playbook /vagrant/springboot.yaml --ask-pass
'''
      }
    }

  }
}