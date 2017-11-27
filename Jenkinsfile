pipeline {
 	// Clean workspace before doing anything
    deleteDir()

    agent any
    tools { 
        maven 'Maven 3.5.2' 
        jdk 'jdk8' 
    }

    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

        stage ('Build') {
            steps {    
                sh "echo 'shell scripts to build project...'"
                sh 'mvn clean package'
            }
        }
    }
}