node(){

	
	stage('Build') 
	{
		try 
		{ 
			def mvnHome = tool 'Maven_Linux'
      sh "set path=C:\\maven\\apache-maven-3.6.2\\bin"
       sh "set path=C:\\Program Files\\Java\\jdk1.8.0_45\\bin"
			
			sh "mvn -version"
      sh "java -version"
			sh "mvn -U clean install -Dmaven.test.skip=true"
			currentBuild.result = 'SUCCESS'
		}
		catch (any) 
		{
			currentBuild.result = 'FAILURE'
			throw any
		} 
	
	}
    
}
