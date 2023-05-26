
node{
  def app

    stage('Clone') {
	checkout scm
    }

    stage('Build Image') {
	app = docker.build("momo/nginx")
    }

    stage('Run Image') {
	docker.image('momo/nginx').withRun('-p 80:80') { c ->

	sh 'docker ps'

	sh 'curl localhost'

	}

	}

}
