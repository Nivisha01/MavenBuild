node(){

	
	stage('Code Checkout'){
		git branch: 'master' , url: 'https://github.com/Nivisha01/MavenBuild.git'
	}
	stage('Build Automation'){
		sh """
			ls -lart
			mvn clean install
			ls -lart target

		"""
	}
	stage('Code Deployment'){
		sh "Code Deploy..."
	}
}
