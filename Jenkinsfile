pipeline{
    environment{
         BRANCH_NAME= "${env.BRANCH_NAME}"
	}
    agent any
    tools{
	 gradle 'GRADLE_HOME'
	}

	stages { 
        stage('Clone Repo') {
            steps {
		echo "${BRANCH_NAME}"               
                sh 'rm -rf localzi-andriod-app'                
                sh 'git clone https://github.com/localzi/localzi-andriod-app.git'
            }
        }
	stage('clean and build') {
           steps {
		sh 'gradle -v'
                sh 'gradle clean'
		sh 'gradle build'
            }
	}
    }
}
