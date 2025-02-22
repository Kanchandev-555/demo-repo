pipeline {
   tools{
       jdk 'JAVA_HOME_LINUX'
	   maven 'M2_HOME_LINUX'
	   }
    agent {label 'linuxslave'}

    stages {
        stage('git checkout') {
            steps {
                 git 'https://github.com/Kanchandev-555/demo-repo.git'
                
            }
        }
    
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
		
        stage('test') {
            steps {
                 sh 'mvn test'
            }
        }

        stage('package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}
