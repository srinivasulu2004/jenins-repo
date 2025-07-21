pipeline {
  agent { label 'slave1' }
  stages {
    stage('Build') {
      steps {
        sh 'docker build -t myapp .'
      }
    }
    stage('Run') {
      steps {
        sh '''
        docker stop myapp || true
        docker rm myapp || true
        docker run -d -p 8000:80 --name myapp myapp
        '''
      }
    }
  }
}
