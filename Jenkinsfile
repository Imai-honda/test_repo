pipeline {
    agent none

    options {
      timeout(time:30, unit: 'MINUTES')
      buildDiscarder logRotator(numToKeepStr:'5')
    }

    stages {
        stage("Hell0") {
	    agent {
	      dockerfile {
		filename 'test'
		dir 'Dockerfiles'
		args '-u root'
	      }
	    }

            steps {
              sh 'test.sh'
            }


        }

  
    }

}
