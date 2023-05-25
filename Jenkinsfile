node{
  def app

    stage('Clone') {
        checkout scm
    }

    stage('Build image') {
        app = docker.build("nginx:latest")
    }

    stage('Run image') {
        docker.image('nginx:latest').withRun('-p 30:30') { c ->

        sh 'docker ps'

        sh 'curl localhost'

    }

    }
    
}
