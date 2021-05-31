pipeline {
	agent {
		docker {
			image 'maven:3.8.1-openjdk-17'
			args '-v $HOME/.m2:/root/.m2'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'cd /var/jenkins_home/workspace/Job1/hello_bot'
				sh 'mvn clean install'
				sh 'mvn -X exec:java -Dexec.mainClass=kpi.acts.appz.bot.hellobot.HelloWorldBot -Dexec.args="1601078076:AAGTHF43CyPSXfhi209Zd5CkDe56kJpIN4w vagrantbot"'
			}
		}
	}
}

