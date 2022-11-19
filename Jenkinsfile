pipeline {
  agent { label 'label' }
  stages {
    stage ('BUILD') {
      steps {
        echo "cloning java project from git"
        sh ''' 
		    git clone https://github.com/cpdani14/test2_java.git
	   '''
        }
    }
   stage ('Clone') {
		agent { label 'label' }
		steps {
			echo "Build a binary"
        sh ''' 
			mvn clean package
	   '''
      }
    }
  }
}  
