pipeline {
	agent {
		docker {

			image 'maven:3.8.1-openjdk-17'
			args '-v $HOME/.m2:/root/.m2'
		}
	}
	stages {
		stage('git') {
			steps {
				git url: "https://github.com/Kesha-na-vzlet/appz_bot_example.git"
			}
		}
		stage('Build') {
			steps {
				sh 'mvn clean install'
				sh 'cd /var/jenkins_home/workspace/Lab11/hello_bot'
				sh 'mvn -e exec:java -Dexec.args="1601078076:AAGTHF43CyPSXfhi209Zd5CkDe56kJpIN4w vagrantbot"'
			}
		}
	}
}

