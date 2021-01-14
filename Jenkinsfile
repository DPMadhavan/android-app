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
                sh 'git clone https://$Sakthi_UserName_USR:$Sakthi_UserName_PSW@github.com/localzi/localzi-andriod-app.git'
            }
        }
		stage('clean and build') {
           steps {
                sh './gradlew clean build'
            }
		}
	}
}
