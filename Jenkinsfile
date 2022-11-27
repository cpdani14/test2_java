pipeline {
  agent { label 'label1' }
  stages {
    stage ('CLONE') {
      steps {
        echo "cloning java project from git"
        	git branch: 'main', url: 'https://github.com/cpdani14/test2_java.git'
        }
    }
   stage ('BUILD') {
		agent { label 'label1' }
		steps {
			echo "Build a binary"
        sh ''' 
			mvn clean package
	   '''
      }
    }
  }
}  
