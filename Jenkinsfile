pipeline{
    environment{
		BRANCH_NAME= "${env.BRANCH_NAME}"
	}
    agent any
	stages { 
        stage('Clone Repo') {
            steps {
		    echo "${BRANCH_NAME}"               
                sh 'rm -rf localzi-andriod-app'                
                sh 'git clone https://github.com/DPMadhavan/andriod-app.git'
            }
        }
		stage('clean and build') {
           steps {
                sh './gradlew clean build'
            }
		}
	}
}
