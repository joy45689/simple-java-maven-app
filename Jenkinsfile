pipeline {
    agent any
	node{
		if (isUnix()) --> sh "command"
		else --> bat "command"
	}
    stages {
        stage('Build') { 
            steps {
                command 'mvn -B -DskipTests clean package' 
            }
        }
    }
}